# My BIOS-settings

Some BIOS-settings are recommended for the Z490 platform in general, and some BIOS-settings depend on wether you use the iMac20,2 or the iMacPro1,1 config.

## Disable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#disable):
- Fast Boot
- Secure Boot
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Intel SGX
- Intel Platform Trust
- CFG Lock (requires a newer BIOS version F5 (This must be off, if you can't find the option then enable both AppleCpuPmCfgLock and AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

## Enable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#enable):
- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI

## Thunderbolt
- GPIO Force Power: Enabled
- Security: No security

## iMac20,2-specific settings:
- Primary Graphics Adapter: PCIE (when you plugin the monitor in the graphics card) or iGPU (when you plugin the monitor to your onboard HDMI)
- Share Memory: 64MB
- IGPU Multi-Monitor: Enabled (this keeps the iGPU enabled even when a graphics card is detected)

## iMacPro1,1-specific settings:
- Primary Graphics Adapter: PCIE (with iMacPro1,1 config, the iGPU is disabled)
- Share Memory: 64MB
- IGPU Multi-Monitor: Disabled (iGPU is disabeld when a graphics card is detected)

Here are screenshot of the most relevant BIOS-settings.

I am not saying that you have to set every setting exactly like I did. Just so you know what works for me :).

This guide was written with mother board BIOS version number "F3", but others have reported that BIOS version "F5" (the latest at time of writing) works equally well. (It is presumed that BIOS version "F4" would also work equally well.)

![My BIOS-setting 2](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0117.jpg)

![My BIOS-setting 3](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0118.jpg)

![My BIOS-setting 4](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0119.jpg)

![My BIOS-setting 5](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0120.jpg)

![My BIOS-setting 6](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0121.jpg)

![My BIOS-setting 7](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0122.jpg)

![My BIOS-setting 8](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0123.jpg)

![My BIOS-setting 9](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0124.jpg)

![My BIOS-setting 10](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D/blob/master/BIOS-settings/IMG_0124.jpg)


