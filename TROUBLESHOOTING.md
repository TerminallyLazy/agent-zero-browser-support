# Understand connection status

| What you see | What it means | Next step |
| --- | --- | --- |
| Companion not detected | Chrome cannot reach its local companion. | Install the host package on the Chrome computer, not inside Docker. Check that the package matches the extension channel. |
| Local host detected | Native messaging is working. | Pair once if no saved pairing is shown. This is not yet browser-control readiness. |
| Development identity paired | The profile has a saved development identity. | Select that browser for the chat in Agent Zero, then reconnect after selection if prompted. |
| Browser control is off | Pairing exists but the server has not admitted this browser runtime. | Check the selected chat/browser and server setup. Repeated pairing does not enable missing server support. |
| Limited control ready | The preview's bounded browser operations are admitted. | Allow a site in Agent Zero and begin an owned-tab task. Chat, screenshots, clicking, typing, and upload remain unavailable in this preview. |
| Disconnected or reconnecting | The companion/server connection was lost. | Verify that the Agent Zero address still opens. Allow the connection to recover; use the offered reconnect action if it remains inactive. |

**Check again / Refresh control status only reads status.** It does not install
software, select a browser, enable the server runtime, or reconnect an inactive
development pairing. An unchanged result can be accurate, rather than a failed
button.

After a pairing timeout, check the saved-pairing status before trying another
code: the server may have accepted the first attempt even if its reply was lost.
An expired or definitively rejected code can be regenerated in Agent Zero.

Do not routinely uninstall, delete credentials, disable browser security,
disable macOS security protections, or share secrets to fix a connection.

For help, [open an issue](https://github.com/TerminallyLazy/agent-zero-browser-support/issues/new)
with the exact status wording and version numbers. Public issues must not
contain pairing codes, credentials, private page content, or unredacted logs.
