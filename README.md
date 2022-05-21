# ISW Modern
<img src="https://github.com/FaridZelli/ISW-Modern/blob/master/image/isw.svg" alt="" width="25%" align="right">
   
A fork of https://github.com/YoyPa/isw with some improvements   
Many thanks to [BeardOverflow](https://github.com/BeardOverflow/isw) for the ec_sys fixes
   
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
For other distros, see the [original instructions](https://github.com/YoyPa/isw#how-to-install). (May or may not work)
   
---
   
## FAQ:
- **Q:** Why ISW-Modern?   
**A:** I originally started looking into ISW for my MSI Modern 15, hence the name.

- **Q:** Is this a revival of ISW?   
**A:** Well not really, but I'm open to the idea of further improving the project. Have a suggestion? Make a pull request, or start a discussion!

- **Q:** Is the original project dead?   
**A:** I don't know, but it's been unmaintained since 2020 and has recently become unusable due to the ```ec_sys``` kernel module which has been missing on many distros lately.

- **Q:** My laptop exploded!   
**A:** That's on you man.
   
---
   
## Useful resources:
- https://github.com/BeardOverflow/isw   
- https://github.com/YoCodingMonster/OpenFreezeCenter   
- https://github.com/nbfc-linux/nbfc-linux   
- https://github.com/musikid/acpi_ec   
- https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=980555
   
---
   
Fun fact: Turning off your laptop fans can improve battery life by up to 2 Hours on a well setup system.
