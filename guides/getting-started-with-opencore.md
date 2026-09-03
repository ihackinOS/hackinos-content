# Getting Started with OpenCore

OpenCore is a bootloader used to start macOS on compatible non-Apple hardware. A reliable setup begins with accurate hardware information and a carefully prepared EFI folder.

## Start with a hardware inventory

Before selecting kexts, ACPI patches, or an SMBIOS model, identify:

- CPU generation and exact model
- Motherboard or laptop model
- Integrated and discrete graphics
- Ethernet and wireless chipset
- Storage controller mode
- Target macOS version

## EFI folder basics

A typical OpenCore EFI has this structure:

```text
EFI/
├── BOOT/
│   └── BOOTx64.efi
└── OC/
    ├── ACPI/
    ├── Drivers/
    ├── Kexts/
    ├── OpenCore.efi
    └── config.plist
```

> Never replace a working EFI folder without keeping a tested backup.