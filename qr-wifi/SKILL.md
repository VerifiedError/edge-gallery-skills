---
name: qr-wifi
description: Generate a QR code that auto-joins a Wi-Fi network when scanned.
---

# Wi-Fi QR Code

This skill generates a QR code that a phone camera can scan to automatically join a Wi-Fi network.

## Examples

- "Make a QR code for my Wi-Fi, SSID HomeNet, password hunter2"
- "Generate a Wi-Fi QR for the network 'Coffee Shop' with password latte123"
- "Create an open network QR code for 'Lobby'"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields
  - ssid: the network name. Required.
  - password: the network password. Required unless security is `nopass`.
  - security: `WPA` (default), `WEP`, or `nopass` for open networks.
  - hidden: `true` if the SSID is hidden. Default `false`.

If the user hasn't given you a password, ask for it before calling the tool.
