# Agent Zero Browser Bridge

Setup, privacy, and support for the community-maintained Agent Zero browser companion.
This project is maintained by [TerminallyLazy](https://github.com/TerminallyLazy)
and is not an OpenAI product or an official Chrome extension from Google.

## Availability

The signed and notarized **macOS companion 2.12.3** is
[available publicly](https://github.com/TerminallyLazy/agent-zero-browser-releases).
Its native installation and installed-state checks passed on Apple Silicon.
The Chrome Web Store item remains a draft. [Download the guided extension ZIP](https://github.com/agent0ai/agent-zero-browser-extension/releases/download/extension-v0.1.1-prestore/agent-zero-browser-0.1.1-unpacked.zip)
and extract it, then open START-HERE.html. Windows and Linux native packages
are not yet released. The required [Core integration](https://github.com/agent0ai/agent-zero/pull/1877)
and [CLI/native integration](https://github.com/agent0ai/a0-connector/pull/26)
are still awaiting maintainer merge; an older Docker image may not contain them.
Do not install a similarly named extension assuming it belongs to this project.

The production extension has its own identity and pairing. Older packages
marked Development remain a separate limited preview; they are not upgraded
to production by changing their display text. Follow the setup guide for the
channel you actually installed. Source and package checks do not establish
that a particular browser session has been admitted for control.

## Start here

- [Installation and one-time pairing](SETUP.md)
- [Connection troubleshooting](TROUBLESHOOTING.md)
- [Privacy and data handling](PRIVACY.md)
- [Get help or report a problem](https://github.com/TerminallyLazy/agent-zero-browser-support/issues/new)

The companion belongs on the computer running Chrome. This is true even when
Agent Zero runs in Docker or on another server. Updating the companion normally
keeps the saved pairing; uninstalling and pairing again is not a routine repair.

## Reporting safely

Issues in this repository are public. Include the operating system, Chrome and
extension versions, and the exact connection-status wording. Do not include a
pairing code, API key, cookie, private URL, chat transcript, screenshot containing
private information, or unredacted logs. For a sensitive report, ask the
maintainer for a private channel before sending details.

This repository contains support documentation only. The
[extension source repository](https://github.com/agent0ai/agent-zero-browser-extension)
is public; neither repository includes companion credentials or Agent Zero user data.
