# Dell Latitude 7490 OpenCore EFI Guide

This guide covers the included EFI configuration, BIOS preparation, supported features, and installation notes for the Dell Latitude 7490.

## Hardware profile

| Component | Configuration |
|---|---|
| CPU | Intel Core i5-8350U |
| Graphics | Intel UHD 620 |
| Platform | Laptop |
| macOS | Ventura and Sonoma |

## BIOS settings

Before installing macOS, review the following settings:

- Disable Secure Boot.
- Disable Fast Boot where available.
- Set SATA mode to AHCI.
- Enable UEFI boot mode.
- Disable unsupported virtualization or legacy boot options only when required by your configuration.

## What works

- Internal display acceleration
- Audio
- Sleep and wake
- Bluetooth
- Compatible Wi-Fi hardware

## Important notes

> Back up your current EFI folder and `config.plist` before replacing anything.

Do not use this EFI without verifying that your hardware matches the listed model and specifications.