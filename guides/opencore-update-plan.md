# How to Create a Safe OpenCore Update Plan

Updating OpenCore, kexts, ACPI patches, or `config.plist` without a recovery plan can leave a system unable to boot. This guide explains a safer update workflow.

## Before updating

- Create a full backup of the current EFI folder.
- Keep a working USB recovery EFI.
- Record the current OpenCore version and macOS version.
- Read the changelog for OpenCore and every kext you plan to update.
- Validate `config.plist` before rebooting.

## Recommended workflow

1. Mount the EFI partition.
2. Duplicate the active EFI folder to a dated backup location.
3. Update one group of components at a time.
4. Run `ocvalidate` against the updated `config.plist`.
5. Test booting with the recovery USB before replacing the internal EFI.
6. Keep the previous known-good EFI until the new version has been tested.

## Recovery considerations

> Never make major EFI changes without a tested fallback boot option.

If a change causes a boot failure, use the recovery USB to start macOS, mount the internal EFI partition, and restore the previous working configuration.