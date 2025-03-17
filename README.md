# EFI for Ryzen 3 3200g with AMD Radeon™ Vega 8 Graphics

## Specifications:

- Motherboard: Gigabyte™ A320M-S2H (rev. 1.x)
- CPU: AMD Ryzen™ 3 3200G, 3.6GHz
- APU: AMD Radeon™ Vega 8 Graphics
- Memory: DDR4 32GB Kingston (KVR26N19D8/16 x2)
- Audio Codec: Realtek® Audio CODEC ALC887
- Ethernet: Realtek® GbE Family LAN
- Storage: Kingston NV2, M.2 2280 PCIe (1TB)
- Opencore: v1.0.4

**Important Notice:**

- You must generate and apply a valid SMBIOS!

- Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate appropriate SMBIOS values for your system.

- Open your config.plist using [ProperTree](https://github.com/corpnewt/ProperTree)

BIOS Settings:

Disable:

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- Above 4G Decoding
	- This must be off, because it doesn't work (in this case) with Nootedred.kext.
- Compatibility Support Module (CSM).
    - If the boot keeps looping, it's probably that.
- CFG Lock (MSR 0xE2 write protection)
	- This must be off, if you can't find the option then ENABLE AppleXcpmCfgLock.
	- Your hack will not boot with CFG-Lock enabled.
	- For 10.10 and older, you'll need to ENABLE AppleCpuPmCfgLock as well.

Enable:

- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- SATA Mode: AHCI
