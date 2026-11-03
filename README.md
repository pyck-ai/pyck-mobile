<p align="center">
  <img src="assets/app-icon.png" width="96" height="96" alt="Pyck app icon">
</p>

# Pyck Mobile App

Android releases of the **Pyck Mobile App**, the handheld companion to the
[Pyck](https://pyck.ai) platform for inventory and workflow management. Scan
barcodes and QR codes with your phone camera or a dedicated scanner device,
run the workflows configured for your organisation and keep working while
you are offline.

This repository only distributes the app. It contains no source code, and
nothing here needs to be built. If you are looking for the latest version,
go straight to the **[Releases](../../releases/latest)** page.

## Download

Every release comes with one file, `pyck-vX.Y.Z.zip`, attached to the
[latest release](../../releases/latest). The zip contains the signed Android
package `pyck-vX.Y.Z.apk`. It is zipped because many mail gateways and
corporate proxies block bare `.apk` downloads.

The release notes below each release list what changed in that version.

## Requirements

- Android 8.0 (API level 26) or newer
- A camera, for scanning with the phone camera
- Supported scanner devices with hardware triggers, such as Zebra and Honeywell
  handhelds, work out of the box

## Installation

1. Download `pyck-vX.Y.Z.zip` from the release page.
2. Unzip it and open `pyck-vX.Y.Z.apk` on the device.
3. If asked, allow installing apps from this source. Android asks once per
   app you install from, such as your browser or file manager.
4. Confirm the installation and open **Pyck**.

### Updating

Install the new version the same way, over the existing one. Your login and
settings are kept. Android verifies that the update is signed with the same
key as the installed app; the installer refuses anything else, so an update
can never be swapped for a foreign build.

### Managed devices (MDM / EMM)

For fleet-wide roll-outs, upload the `.apk` from inside the zip to your
device management system. The package name is `ai.pyck.mobile`.

Every release is signed with the same Pyck release certificate. Its SHA-256
fingerprint, for allow-lists and verification:

```
FF:7C:CB:50:F8:98:97:72:DC:70:CA:7A:6D:84:C1:FA:A9:AF:7F:5D:3A:0F:EB:58:94:A7:74:88:2E:A9:D2:7C
```

You can check it yourself with `apksigner` from the Android build tools:

```bash
apksigner verify --print-certs pyck-vX.Y.Z.apk
```

## Releases and versions

- Versions follow `vMAJOR.MINOR.PATCH`. The release marked **Latest** is the
  one to install.
- Tags with a suffix, such as `v1.3.1-rc1`, are **pre-releases**: test
  builds that are never marked as latest and never announced by e-mail.
  Install them only when the Pyck team asks you to.
- Releases are immutable. Once published, a release and its file never
  change. A correction always ships as a new version.

## Release notifications

Customers receive an e-mail from **Pyck \<noreply@pyck.cloud\>** whenever a
new version is published. It contains the release notes and the download
link. Every mail has an unsubscribe link in the footer. To add or remove
addresses for your organisation, write to [hello@pyck.ai](mailto:hello@pyck.ai).

## Feedback and support

Something missing, something broken, or an idea for the next release?
Write to [hello@pyck.ai](mailto:hello@pyck.ai). Every message is read by the
team.

---

© Pyck. The Pyck Mobile App is proprietary software for Pyck customers.
Redistribution outside your organisation is not permitted.
