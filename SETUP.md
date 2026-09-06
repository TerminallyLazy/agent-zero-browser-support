# Install and connect once

These instructions describe production-channel setup. The Chrome Web Store
item is still a draft, so installing the supplied extension currently requires
one manual Chrome step. Windows and Linux release packages are not yet available.

## 1. Install on the Chrome computer

On macOS 13 or later, download the corrected
[Agent Zero Browser Setup](https://raw.githubusercontent.com/TerminallyLazy/agent-zero-browser-releases/native-v2.12.0-macos-r2/v2.12.0/a0-browser-bridge-2.12.0-macos-universal2.dmg).
Open the disk image, open **Agent Zero Browser Setup**, then choose
**Install browser companion**. No administrator password is needed.

This Mac package is signed and notarized. If macOS blocks it, do not disable
Gatekeeper or remove quarantine attributes; report the message to the maintainer.

If you run Agent Zero in Docker, leave the companion on your normal computer;
do not run this installer inside the container.

For the maintainer-supplied production extension, open Chrome's Extensions page, enable Developer mode,
choose **Load unpacked**, and select the extension folder from the supplied
package. Its name is **Agent Zero Chrome Bridge**, without a Development suffix,
and its ID is `nhliclifilepdkoolioacpjpijomfplj`. Chrome's Developer mode switch
allows the unpacked install; it does not change this package's production identity.

## 2. Pair with your Agent Zero

1. In Agent Zero, open **Browser settings → Chrome extension**.
2. Create a pairing code and copy it. Codes expire after five minutes.
3. Open the extension's Options. Enter your Agent Zero address and paste the code,
   then choose **Pair this browser**. For a Docker instance on the same computer,
   use the address that already opens Agent Zero in Chrome.
4. Return to Agent Zero and select this browser for the chat.
5. Connection checks retry automatically. You can close Options; no new code is needed.

Pairing is saved for this Chrome profile. You should not need a new code every
time you open Chrome, open the side panel, start a chat, or update the companion.
Choosing which browser a chat uses and approving a new site are separate from
pairing. Do not paste your code into a support issue or chat.

## 3. Check the result

Options should show the extension, local companion, and saved pairing as ready.
The browser runtime must separately report that browser control is ready.
A successful pairing alone does not enable browser control.

Allow the exact site in Agent Zero's Browser settings before asking it to work
there. Agent-owned tabs appear in a labeled group. Your other tabs are not
implicitly shared. Taking over an owned tab stops the agent's control of it;
uncertain or user-owned tabs are kept open instead of being closed automatically.

## Updating

Use the supplied installer/update entry point. Keep the same Chrome profile.
Do not choose **Disconnect profile**, revoke the browser, or delete its saved
credentials just to update. An unpacked extension may need **Reload** on Chrome's
Extensions page after its files change.

If a connection step fails, use the [status guide](TROUBLESHOOTING.md) before
creating a new pairing code.

## Existing Development packages

Development packages retain their separate identity, credentials and limited
browser actions. Keep their saved pairing intact; do not relabel them or copy
credentials into production. Moving to the production extension requires one
new production pairing. Ordinary updates within that production profile preserve it.
