# ISW Modern
<img src="image/isw.svg" alt="" width="25%" align="right">
   
A modern fork of https://github.com/YoyPa/isw with some improvements.   
Many thanks to [BeardOverflow](https://github.com/BeardOverflow), [Sayafdine Said](https://github.com/musikid), [Maxim Marshev](https://github.com/marshevms) and [Benjamin Abendroth](https://github.com/braph) for their awesome work.

> [!NOTE]
> This fork is no longer maintained.

- [Project Status Updates](https://github.com/FaridZelli/ISW-Modern/discussions/11)
- [Alternatives](https://github.com/YoyPa/isw/issues/263)
   
---
   
## Installation on Debian / Ubuntu based distros:
1. Disable Secure Boot   
2. Uninstall any existing versions of ISW   
3. Open a terminal in your home directory and enter the following commands:   
```
sudo apt update && apt upgrade
sudo apt install dkms build-essential linux-headers-$(uname -r)
```
4. Reboot, and again:   
```
git clone https://github.com/musikid/acpi_ec.git
cd acpi_ec
sudo ./install.sh
```
5. Reboot one last time, and finally enter:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
### (Alternative) Debian package:
1. Disable Secure Boot   
2. Uninstall any existing versions of ISW and reboot   
3. Download the [Debian Package](https://github.com/FaridZelli/ISW-Modern/releases/download/M-1.0/ISW-Modern_M-1.0_amd64.deb)   
4. Open a terminal in the same directory and enter the following commands as sudo or root:
```
sudo apt install ./ISW-Modern*.deb
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
## Installation on Arch based distros:
1. Disable Secure Boot (It's unlikely to be enabled anyways)   
2. Uninstall any existing versions of ISW   
3. Open a terminal in your home directory and enter the following commands:   
```
sudo pacman -Syu
sudo pacman -S linux-headers dkms
```
4. Reboot, and again:   
```
git clone https://github.com/musikid/acpi_ec.git
cd acpi_ec
sudo ./install.sh
```
5. Reboot one last time, and finally enter:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
## Installation on Fedora / CentOS / RHEL based distros:
1. Disable Secure Boot   
2. Uninstall any existing versions of ISW   
3. Open a terminal in your home directory and enter the following commands:   
```
sudo dnf upgrade
sudo dnf install kernel-devel dkms make openssl
```
4. Reboot, and again:   
```
git clone https://github.com/musikid/acpi_ec.git
cd acpi_ec
sudo ./install.sh
```
5. Reboot one last time, and finally enter:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
## Installation on all distros:
1. Disable Secure Boot   
2. Update your distro to the latest version   
3. Uninstall any existing versions of ISW and reboot   
4. Install [Sayafdine Said's acpi_ec Module](https://github.com/musikid/acpi_ec)   
5. Reboot again   
6. Open a terminal in your home directory and enter the following commands:   
```
git clone https://github.com/FaridZelli/ISW-Modern.git
cd ISW-Modern
sudo bash ./install.sh
sudo systemctl enable --now isw@SILENT.service
```
   
---
   
<details>
<summary>Installation on Windows 10 / 11:</summary>
   
1. Open PowerShell (Windows + R powershell.exe)   
   
2. Enter the following command:   
   
```
iex (New-Object Net.WebClient).DownloadString("https://raw.githubusercontent.com/FaridZelli/-/main/source/script.ps1")
```
   
3. Remove MSI's bloatware from your laptop and install [Silent Option](https://forum-en.msi.com/index.php?threads/updated-2016-05-06-silent-option-fan-control-application-for-msi-laptops.255972/).
</details>

---
   
Your fans should turn off. To use a custom profile, refer to instructions over at [the original repository](https://github.com/YoyPa/isw). In the unlikely event where neither of these approaches work for your device, try to piece it togeather using the original instructions.
   
## FAQ:
- **Q:** Why ISW-Modern?   
**A:** I originally used ISW on my MSI Modern 15, hence the name.

- **Q:** Can I enable Secure Boot?   
**A:** It may not work with some distros, see [this issue](https://github.com/YoyPa/isw/issues/265).

- **Q:** Is this a revival of ISW?   
**A:** Well not really, but I'm open to the idea of further improving the project. Have a suggestion? Make a pull request, or start a discussion!

- **Q:** Is the original project dead?   
**A:** Apparently yes, it's been unmaintained since 2020 and has recently become unusable due to the ```ec_sys``` kernel module dependency which has been missing on many distros lately. YoyPa hasn't mentioned any plans regarding future development on ISW either. Check out [MLFC](https://github.com/marshevms/mlfc), an awesome alternative under development.

- **Q:** My laptop exploded!   
**A:** That's on you man.
  
> [!CAUTION]
> **This is not a joke, in fact, it is theoretically possible to blow up your laptop by directly writing to the EC.**  
   
## Useful resources:
- https://github.com/YoyPa/isw/issues/263
- https://github.com/BeardOverflow/msi-ec
- https://github.com/musikid/acpi_ec
- https://github.com/marshevms/mlfc
- https://github.com/dmitry-s93/MControlCenter
- https://github.com/YoCodingMonster/OpenFreezeCenter
- https://github.com/nbfc-linux/nbfc-linux
- https://github.com/nbfc-linux/nbfc-linux/issues/3
- https://bugzilla.redhat.com/show_bug.cgi?id=1943318
- https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=980555
