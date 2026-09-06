# Agent Zero Browser Bridge

Setup, privacy, and support for the community-maintained Agent Zero browser companion.
This project is maintained by [TerminallyLazy](https://github.com/TerminallyLazy)
and is not an OpenAI product or an official Chrome extension from Google.

## Availability

The signed and notarized **macOS companion 2.12.0 (r2)** is
[available publicly](https://github.com/TerminallyLazy/agent-zero-browser-releases).
Its native installation and installed-state checks passed on Apple Silicon.
The Chrome Web Store item remains a draft; full live production browser
acceptance is still pending. Windows and Linux packages are not yet released.
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

This repository contains support documentation only. It does not redistribute
the private extension source, companion credentials, or Agent Zero user data.
