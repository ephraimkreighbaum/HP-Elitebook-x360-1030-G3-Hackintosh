# HP-Elitebook-x360-1030-G3-Hackintosh
## My EFI folder

## Working:
- Wifi
- Touchscreen
- All USB ports (not Thunderbolt just USB-C)
- iMessage

## Not working:
- Bluetooth
- Camera

Runs macOS Ventura, might spoof for Sonoma support eventually.
EFI is currently OpenCore 1.0.1

all kexts are their latest versions as of Sep 2, 2024


## BIOS

### Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option then enable AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

### Enable

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI

### If available:
- Virtualization Technology (VTx) - Yes
- Virtualization Technology for Directed I/O (VTd) - Yes
- Fast Boot - No
- Video Memory Size - 64 MB
- Intel Management Enginge (ME) - Yes


Credit to [yingw on Github](https://github.com/yingw/HP-Elitebook-X360-1030-G3-Hackintosh/) for his BIOS settings list :)
