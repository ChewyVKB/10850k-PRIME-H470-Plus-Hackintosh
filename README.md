# 10850k-PRIME-H470-Plus-Hackintosh

Hey everyone! I've managed to build a pretty stable hack using an 
10850k on an Asus PRIME H470-Plus with an RX 580

Feel free to take a look at my EFI for reference on your soon-to-be hack!

# Version
- __OpenCore v0.9.3__
- __SMBIOS iMac Pro 1,1__

Supports

- __Ventura 13.x__
- __Sonoma (kind of)__ certain iServices will not work. (Mainly just Facetime, with some delayed iMessage functions)

Hack setup was made following the documentation over at https://dortania.github.io/OpenCore-Install-Guide/
- __⚠️ Be sure to follow the guide closely as your system may differ from mine slightly. Only use this as a reference while building.__

# Hardware Used

| Component  | Details |
| ------------- | ------------- |
| Motherboard  | Asus PRIME H470-Plus  |
| CPU  | Intel 10850k  |
| iGPU  | Intel 10850k (UHD 630 Headless)  |
| dGPU  | rx 580 (for now. Will upgrade to 6800XT soon.  |
| RAM  | 128gb Kingston FURY (3200MT/s DDR4)  |
| MB Audio  | Realtek® ALC887  |
| MB Ethernet  | Realtek® RTL8111H  |
| Wifi  | None yet. Will update soon.  |
| Storage  | Crucial P3 1TB NvME m.2  |

# Firmware Drivers
1. AudioDxe
    - (__Optional__) Used to get BootChime. Just be sure to follow the instructions on Opencore's Post Install Guide.
2. HfsPlus
   - (__Required__) You can try OpenHfsPlus provided by opencore if you are having problems with this. May or may not work.
3. OpenCanopy
   - (__Optional__) This is for adding a GUI to opencore's bootloader. Make sure to follow the instructions on Opencore's Post Install Guide.
4. OpenRuntime
   - (__Required__)
5. ResetNvramEntry
   - (__Not necesarily required, but using this will make your life a lot easier.__) Use this to Reset NVRAM.

# Kexts
__There are two Kexts below that you may not need for this build. Many users are saying that they don't use them, but I have yet to test this.__ _RadeonSensor_ and _SMCRadeonGPU_.
- AppleALC
- Lilu
- RadeibSebsir
- ReaktekRTL8111
- SMCProcessor
- SMCRadeonGPU
- SMCSUuperIO
- USBMap  (_I'm having a few issues mapping on the H470-Plus. I still need to tinker with these settings._)
- VirtualSMC
- WhateverGreen

# SSDTs
__I should note that I dumped my DSDT and created these manually. These may not work for your specific system.__
- SSDT-AWAC
- SSDT-EC-USBX
- SSDT-PLUG
