# Password Wallet — management page

Browser panel for a [password-paster-esp32](https://github.com/) device:
an ESP32-S3 USB password wallet with a touchscreen.

Open the hosted page in **Chrome or Edge** (WebHID exists nowhere else),
press **Connect**, and pick the device.

## What it can and cannot do

The device deliberately limits this page:

- **Stored passwords are never sent back.** There is no export command in
  the protocol, so the list shows names and usernames only. Editing a
  password means overwriting it.
- **Every change needs a tap on the device.** The page asks; the device
  puts the question on its own screen and waits for a human. Software on
  the PC can send any command it likes, but it cannot press Confirm.

## Pairing

Press **Use this page for Settings** and confirm on the device. After
that, the Settings button on the device opens this page on whatever PC
it is plugged into.

The device stores only the host and path — never the scheme — and
prepends `https://` itself, accepting only `[A-Za-z0-9._~/]`. That is
why a `file://` copy cannot pair: a local path is machine-specific, and
`file://` is the form that could launch a local program rather than open
a page.

## Hosting

One static file with no build step and no dependencies. GitHub Pages:
repo **Settings → Pages → Deploy from a branch → `main` / root**.
