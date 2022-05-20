# ISW Modern
<img src="https://github.com/FaridZelli/ISW-Modern/blob/master/image/isw.svg" alt="" width="25%" align="right">
   
### A fork of https://github.com/YoyPa/isw with minor improvements
### Many thanks to [BeardOverflow](https://github.com/BeardOverflow/isw) for ec_sys fixes
   
---
   
- **Installation on Debian based distros:**   
> Disable Secure Boot   
> Uninstall / remove any existing versions of ISW and reboot   
> Download the [Debian Package](https://github.com/FaridZelli/ISW-Modern/releases/download/M-1.0/ISW-Modern_M-1.0_amd64.deb)   
> Open a terminal in the same directory and enter the following commands as sudo or root:
```
sudo apt install ./ISW-Modern*.deb
sudo systemctl enable --now isw@SILENT.service
```

Your fans should turn off. To use a custom profile, refer to instructions over at [the original repository](https://github.com/YoyPa/isw).
   
---
   
## FAQ:
- **Q:** Is this a revival of ISW?   
**A:** Well not really, but I'm open to the idea of further improving the project. Have an idea? Make a pull request, or start a discussion!

- **Q:** Is the original project dead?   
**A:** I don't know, but it's been unmaintained since 2020 and has recently become nearly unusable due to the ```ec_sys``` module which has been missing on many distros lately.

- **Q:** My laptop exploded!   
**A:** That's on you man.
   
---
   
## Useful resources:
- https://github.com/BeardOverflow/isw   
- https://github.com/YoCodingMonster/OpenFreezeCenter   
- https://github.com/nbfc-linux/nbfc-linux   
- https://github.com/musikid/acpi_ec   
- https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=980555
