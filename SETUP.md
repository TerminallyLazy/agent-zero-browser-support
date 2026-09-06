# Install and connect once

These instructions describe the current limited development preview. It is not
yet a one-click store installation. Only use a preview package supplied by this
project's maintainer; no public production download is available yet.

## 1. Install on the Chrome computer

Download and extract the package for your computer. On macOS, open
`Install.command`. On Linux, follow the included `START-HERE` instructions for
`install.sh`. Windows installer availability has not been verified.

If macOS blocks the preview, do not disable Gatekeeper or run commands to remove
quarantine attributes. The preview is not a notarized production installer.
Report the message to the maintainer.

If you run Agent Zero in Docker, leave the companion on your normal computer;
do not run this installer inside the container.

For the preview extension, open Chrome's Extensions page, enable Developer mode,
choose **Load unpacked**, and select the extension folder from the supplied
package. This manual step is specific to the development preview.

## 2. Pair with your Agent Zero

1. In Agent Zero, open **Browser settings → Development browser companion**.
2. Create a development pairing code and copy it. Codes expire after five minutes.
3. Open the extension's Options. Enter your Agent Zero address and paste the code,
   then choose **Pair this browser**. For a Docker instance on the same computer,
   use the address that already opens Agent Zero in Chrome.
4. Return to Agent Zero and select this development browser for the chat.
5. If Options says to reconnect after selection, choose **Reconnect after selection**.

Pairing is saved for this Chrome profile. You should not need a new code every
time you open Chrome, open the side panel, start a chat, or update the companion.
Choosing which browser a chat uses and approving a new site are separate from
pairing. Do not paste your code into a support issue or chat.

## 3. Check the result

Options should show the extension, local companion, and saved pairing as ready.
The development browser runtime must separately report **limited control** as
ready. A successful pairing alone does not enable browser control.

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
