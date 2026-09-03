# EFI Backup and Recovery

EFI changes can prevent a Hackintosh from booting. Keep an external recovery USB and a verified copy of the current EFI before updating OpenCore, kexts, ACPI patches, or `config.plist`.

## Recommended backup workflow

1. Mount the EFI partition.
2. Copy the complete `EFI` folder to a dated backup location.
3. Keep an additional copy on a USB drive.
4. Record the OpenCore version, macOS version, and important changes.
5. Test major changes before deleting the previous working version.

## Recovery USB

A recovery USB should contain a known working EFI configuration. It can boot the machine if an update breaks the internal EFI.

## Validate before rebooting

Use ProperTree, OCValidate, and relevant documentation to validate important changes before restarting.