# Install and connect once

The Chrome Web Store item is still a draft. The supplied **unpacked ZIP** includes
an offline **START-HERE.html** guide and a ready-to-load extension folder. No
Node, Rust, terminal, or source build is needed to load it. The separate
**store-candidate ZIP** is only for the developer dashboard.

| Chrome computer | Extension | Native companion |
| --- | --- | --- |
| macOS 13+, Intel / Apple Silicon | Same unpacked ZIP | Signed/notarized 2.12.3 installer available |
| Windows | Same unpacked ZIP | Installer and native platform verification incomplete |
| Linux x86-64 / ARM64 | Same unpacked ZIP | Candidate builds exist; production installer not released |

**Windows and Linux end-to-end browser control is not available yet.** Loading
the extension alone does not provide a native companion. Do not use the Mac
installer, WSL, or a Docker container as a replacement. Conventional desktop
Chrome and Secret Service are required for the Linux companion; Snap/Flatpak
integration is not supported.

## 1. Install on the Chrome computer

On macOS 13 or later, download the corrected
[Agent Zero Browser Setup 2.12.3](https://raw.githubusercontent.com/TerminallyLazy/agent-zero-browser-releases/native-v2.12.3-macos/v2.12.3/a0-browser-bridge-2.12.3-macos-universal2.dmg).
Open the disk image, open **Agent Zero Browser Setup**, then choose
**Install browser companion**. No administrator password is needed.

This Mac package is signed and notarized. If macOS blocks it, do not disable
Gatekeeper or remove quarantine attributes; report the message to the maintainer.

If you run Agent Zero in Docker, leave the companion on your normal computer;
do not run this installer inside the container.

Extract the entire supplied ZIP first: use **Extract All** on Windows, open the
ZIP on macOS, or use the desktop archive manager on Linux. Keep the extracted
folder somewhere permanent, such as Documents—not in a ZIP preview or temporary
directory. Open **START-HERE.html** for the guided steps.

In your normal Chrome profile, open `chrome://extensions`, enable **Developer
mode**, choose **Load unpacked**, and select the package's **extension** folder
(the one containing `manifest.json`, not its parent). Pin it from Chrome's
Extensions menu if desired. Its name is **Agent Zero Chrome Bridge**, without a Development suffix,
and its ID is `nhliclifilepdkoolioacpjpijomfplj`. Chrome's Developer mode switch
allows the unpacked install; it does not change this package's production identity.
These Chrome steps require the user; no installer should edit browser profiles,
force enterprise policies, or disable OS/browser security to avoid them.

## 2. Pair with your Agent Zero

1. In Agent Zero, open **Browser settings → Chrome extension**.
2. Create a pairing code and copy it. Codes expire after five minutes.
3. Open the extension's Options. Enter your Agent Zero address and paste the code,
   then choose **Pair this browser**. For a Docker instance on the same computer,
   use the address that already opens Agent Zero in Chrome.
4. Return to Agent Zero and choose this browser as the **default** in Browser
   settings. It applies across chats; existing explicit project choices remain unchanged.
5. Connection checks retry automatically. You can close Options; no new code is needed.

Pairing is saved for this Chrome profile. You should not need a new code every
time you open Chrome, open the side panel, start a chat, or update the companion.
Choosing a default browser and granting site access are separate from
pairing. Do not paste your code into a support issue or chat.

## 3. Check the result

Options should show the extension, local companion, and saved pairing as ready.
The browser runtime must separately report that browser control is ready.
A successful pairing alone does not enable browser control.

You can remember individual sites or explicitly enable **All websites** in Agent
Zero's Browser settings to avoid repeated site prompts. Purchases, submissions,
and other consequential actions still need separate approval. Agent-owned tabs
appear in a blue Chrome tab group. Your other tabs are not
implicitly shared. Taking over an owned tab stops the agent's control of it;
uncertain or user-owned tabs are kept open instead of being closed automatically.

## Updating

Use the supplied installer/update entry point. Keep the same Chrome profile.
Do not choose **Disconnect profile**, revoke the browser, or delete its saved
credentials just to update. An unpacked extension may need **Reload** on Chrome's
Extensions page after its files change.
For an extension update, back up the old `extension` folder and replace it with
the new package's `extension` folder at the **same path**, then click **Reload**.
Do not remove the extension from Chrome. Keep the folder after setup; unpacked
extensions do not receive automatic Web Store updates.

If a connection step fails, use the [status guide](TROUBLESHOOTING.md) before
creating a new pairing code.

## Existing Development packages

Development packages retain their separate identity, credentials and limited
browser actions. Keep their saved pairing intact; do not relabel them or copy
credentials into production. Moving to the production extension requires one
new production pairing. Ordinary updates within that production profile preserve it.
