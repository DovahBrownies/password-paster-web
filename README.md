# Password Wallet management page

Browser panel for a personal, self-built USB password wallet: A DIY password hardware wallet that stores credentials to be used on PCs.

**This repo is only useful if you already have that device.** It is a single page that talks to specific custom firmware over WebHID. Without the hardware and the matching firmware there is nothing to run: the page will find no device and do nothing.

## Using it
Open the hosted page in **Chrome or Edge** (WebHID exists nowhere else) and press **Connect**.

## Notes

- Stored passwords are never sent to this page. The list shows names and   usernames only; changing a password means overwriting it.
- Every change is confirmed on the device's own screen, not here.
