# Intune BitLocker Key Backup

PowerShell scripts to ensure that **BitLocker recovery keys are escrowed to Entra ID** for Intune-managed and workplace-joined devices, including legacy or edge-case scenarios where the standard Intune policy did not back the key up successfully.

This repository is published by **PowerStacks** for **BI for Intune** customers and the wider Intune community.

> **Note:** Scripts are being uploaded by the maintainer. When complete the repository will contain the detection and remediation scripts (suitable for use as an Intune Proactive Remediation), plus any helper utilities for the workplace-joined edge case.

**Companion blog post:** [Ensuring BitLocker key backup for workplace-joined devices and beyond](https://powerstacks.com/blog/ensuring-bitlocker-key-backup-for-workplace-joined-devices-and-beyond/)

---

## What's included (planned)

| Script | Purpose |
|--------|---------|
| Detection script | Reports whether the device's BitLocker recovery key has been successfully escrowed to Entra ID |
| Remediation script | Forces a fresh backup of the recovery key to Entra ID for devices flagged by the detection script |
| Workplace-join helper | Handles the legacy workplace-join enrollment path where standard Intune BitLocker policy does not apply |

Each script is intended to be deployed as an Intune Proactive Remediation. Customers can also run them manually for one-off investigations.

---

## Why this matters

Without a successful key escrow, a customer in a recovery scenario (forgotten PIN, motherboard replacement, TPM reset) has no way to unlock the drive and the data is effectively lost. Standard Intune BitLocker policies handle the common case but leave a long tail of devices in inconsistent state. These scripts close that gap.

---

## License

[MIT](LICENSE) - use, modify, and share freely.

## Maintainer

Maintained by **PowerStacks**. Issues and pull requests welcome on the [issue tracker](../../issues).
