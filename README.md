# Muzn Accounts — releases

Installers for **Muzn Accounts**, an offline Windows accounts program for hotels: daily entry, cash and bank
books, baki khata, salary sheet and Excel export.

This repository holds releases only. The source code is kept privately.

## Install

1. Open [the latest release](https://github.com/imamachowdhury/muzn-accounts-releases/releases/latest) and
   download `MuznAccounts-Setup-<version>.exe`.
2. Run it. No admin rights are needed. Windows may say "Windows protected your PC" because the setup is not
   code-signed: click **More info → Run anyway**.

Installed copies (0.3.0 and later) find new releases here by themselves and offer an update to the admin.

## How updates are trusted

Each release carries `latest.json` and `latest.json.sig`. The program installs an update only when the
signature verifies against the publisher's key built into the program, the download link points to a release
in this repository, and the downloaded file matches the signed size and SHA-256. Each release also lists the
installer's SHA-256 so a download can be checked by hand:

```
certutil -hashfile MuznAccounts-Setup-<version>.exe SHA256
```
