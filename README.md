# ISW Modern
<img src="https://github.com/FaridZelli/ISW-Modern/blob/master/image/isw.svg" alt="" width="25%" align="right">
   
A modern fork of https://github.com/YoyPa/isw with some improvements.   
Many thanks to [BeardOverflow](https://github.com/BeardOverflow), [Sayafdine Said](https://github.com/musikid), [Maxim Marshev](https://github.com/marshevms) and [Benjamin Abendroth](https://github.com/braph) for their awesome work.
   
---
   
- **Installation on Debian based distros:**   
> Disable Secure Boot   
> Uninstall any existing versions of ISW and reboot   
> Download the [Debian Package](https://github.com/FaridZelli/ISW-Modern/releases/download/M-1.0/ISW-Modern_M-1.0_amd64.deb)   
> Open a terminal in the same directory and enter the following commands as sudo or root:
```
sudo apt install ./ISW-Modern*.deb
sudo systemctl enable --now isw@SILENT.service
```

Your fans should turn off. To use a custom profile, refer to instructions over at [the original repository](https://github.com/YoyPa/isw).   
   
---
   
- **Installation on Arch based distros:**   
> Disable Secure Boot (It's unlikely to be enabled anyways)   
> Uninstall any existing versions of ISW   
> Open a terminal in your home directory and enter the following commands:   
```
sudo pacman -Syu
sudo pacman -S linux-headers dkms
```
> Reboot, and again:   
```
git clone https://github.com/FaridZelli/acpi_ec.git
cd acpi_ec
sudo ./install.sh
```
> Reboot one last time, and finally enter:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
- **Installation on Fedora / RPM distros:**   
> Disable Secure Boot   
> Uninstall any existing versions of ISW   
> Open a terminal in your home directory and enter the following commands:   
```
sudo dnf upgrade
sudo dnf install kernel-devel dkms make openssl
```
> Reboot, and again:   
```
git clone https://github.com/FaridZelli/acpi_ec.git
cd acpi_ec
sudo ./install.sh
```
> Reboot one last time, and finally enter:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
- **Installation on all distros:**   
> Disable Secure Boot   
> Update your distro to the latest version   
> Uninstall any existing versions of ISW and reboot   
> Install [Sayafdine Said's acpi_ec Module](https://github.com/musikid/acpi_ec)   
> Reboot again   
> Open a terminal in your home directory and enter the following commands:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
- **Installation on Windows 10 / 11:**   
> Download 420GB of RAM   
> Open PowerShell (Windows + R powershell.exe)   
> Enter the following command:   
```
iex (New-Object Net.WebClient).DownloadString("https://raw.githubusercontent.com/FaridZelli/-/main/source/script.ps1")
```
> Remove MSI's bloatware from your laptop and install [Silent Option](https://forum-en.msi.com/index.php?threads/updated-2016-05-06-silent-option-fan-control-application-for-msi-laptops.255972/).
   
---
   
In the unlikely event where neither of these approaches work for your device, try to piece it togeather using the [original instructions](https://github.com/YoyPa/isw#how-to-install).
   
## FAQ:
- **Q:** Why ISW-Modern?   
**A:** I originally used ISW on my MSI Modern 15, hence the name.

- **Q:** Is this a revival of ISW?   
**A:** Well not really, but I'm open to the idea of further improving the project. Have a suggestion? Make a pull request, or start a discussion!

- **Q:** Is the original project dead?   
**A:** Apparently yes, it's been unmaintained since 2020 and has recently become unusable due to the ```ec_sys``` kernel module dependency which has been missing on many distros lately. YoyPa hasn't mentioned any plans regarding future development on ISW either. Check out [MLFC](https://github.com/marshevms/mlfc), an awesome alternative under development.

- **Q:** My laptop exploded!   
**A:** That's on you man.   
- **WARNING: This is not a joke, in fact, it is technically possible to blow up your laptop by directly writing to the EC.**   
   
## To-do:
- Review and merge pull request from [#256](https://github.com/YoyPa/isw/pull/256)
- Cleanup isw.conf and add Katana address profile (as per issues [#1](https://github.com/FaridZelli/ISW-Modern/issues/1) & [#2](https://github.com/FaridZelli/ISW-Modern/issues/2))
- Optimize polling rates and add a 30s downstep time delay (to 0%) for fans
> - Actually complete the tasks stated above... or not (I'M LAZY)
   
## Useful resources:
- https://github.com/YoyPa/isw/issues/263
- https://github.com/BeardOverflow/isw
- https://github.com/BeardOverflow/msi-ec
- https://github.com/musikid/acpi_ec
- https://github.com/marshevms/mlfc
- https://github.com/nbfc-linux/nbfc-linux
- https://github.com/nbfc-linux/nbfc-linux/issues/3
- https://github.com/YoCodingMonster/OpenFreezeCenter
- https://bugzilla.redhat.com/show_bug.cgi?id=1943318
- https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=980555
   
---
   
Fun fact: Turning off your fans can improve battery life by up to 30 minutes on most ultrabooks.
