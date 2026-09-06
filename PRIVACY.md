# Privacy and data handling — Agent Zero Browser Bridge

Last updated: September 5, 2026.

This policy covers this project's Chrome extension and its native browser
companion. The project is maintained by
[TerminallyLazy](https://github.com/TerminallyLazy). Your separately configured
Agent Zero server, its model providers, and the websites you visit have their
own data-handling practices. This extension is not operated by OpenAI or Google.

## What the bridge handles and why

The bridge handles data needed to connect your browser to the Agent Zero
instance you choose and perform the browser tasks you authorize:

- **Connection and pairing:** your chosen Agent Zero address, a short-lived
  pairing code, profile/installation identifiers, and a companion-held signing
  credential. The code is used for pairing, cleared from the input, and is not
  saved in extension storage. The extension does not request an Agent Zero API key.
- **Browser tasks:** approved site origins, navigation addresses, page text and
  semantic page structure, opaque task/tab references, action requests, approval
  decisions, and results. Page content can include personal, health, financial,
  location, authentication, or communication data if present on a page you
  authorize; do not share sites containing information you do not want your
  Agent Zero instance or its configured providers to receive.
- **Local safety records:** connection state, task and tab ownership, identity
  digests, site origins, timestamps, and redacted operation receipts. These
  prevent uncertain actions from being repeated or your unrelated tabs from
  being closed. They are not advertising or general browsing-history records.

The current limited development preview does **not** offer extension chat,
screenshots, clicking, typing, or file upload. The unreleased production
candidate additionally handles selected-chat text and queue previews, approved
screenshots, approved typed text, and explicitly approved current-chat file
attachments. Those data paths are disabled in the limited preview. Selecting a
file for a website can cause that site to upload it immediately; this operation
requires a separate one-use approval in the production candidate.

## Where data goes

Approved task data travels through the local companion to the Agent Zero
server you paired. That server may be on this computer or remote. Your Agent
Zero configuration determines which AI providers or tools subsequently receive
it. Content typed or uploaded to a website also goes to that website according
to the approved operation. Review the server and provider policies before
connecting a browser with sensitive information.

The bridge has no developer-operated analytics, advertising, or telemetry
upload service. It does not send your task data to the maintainer by default,
sell it, use it for advertising, or use it to determine creditworthiness.
Bridge data use and transfer are limited to its user-facing browser-assistance
function. A support report is a separate voluntary disclosure; public GitHub
issues are visible to everyone and are handled under
[GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

The extension does not request access to the Chrome history database, bookmarks,
password store, or cookie API. This does not mean approved page content is free
of sensitive information, or that websites stop using the browser's existing
logged-in sessions.

## Storage and retention

Extension settings and bounded safety records use local Chrome extension
storage, not Chrome Sync. Durable safety records exclude page text, conversation
transcripts, full URL paths/queries/fragments, typed values, and screenshot or
file bytes. They can include site origins and hashed path/identity information.
Completed acknowledged operation records become eligible for cleanup after
seven days; unresolved safety records can remain longer to avoid unsafe replay.
This is not a promise that every local record is erased after seven days.

The native companion keeps its signing credential in the operating system's
credential store, outside extension storage. Authorized file transfers may use
private temporary companion storage in the production candidate. Temporary
transfer cleanup and recovery do not erase the original chat attachment.

Your Agent Zero server can retain chats, attachments, browser results, audit
records, and backups under its own configuration. Closing the extension panel,
disconnecting a profile, or uninstalling the extension does not delete those
server copies or data already sent to websites or AI providers.

## Your controls

Pair only with a server you trust. Select the browser for a chat, control site
access in Agent Zero, and review action approvals. Taking over an agent-owned
tab releases its control. Closing a side panel only closes the viewer; use task
controls to stop work.

Revoke the paired browser in Agent Zero to remove its server authority. In a
supported admitted production connection, the extension's connection-security
controls also request credential revocation. A missing or uncertain server
reply is not treated as successful revocation, and local credentials are kept
until the result can be verified. These production controls are unavailable in
the limited development preview.

Removing the extension removes its Chrome-managed extension data, but does not
uninstall the separate companion or revoke its server identity. Local companion
retirement may keep credentials and recoverable files when cleanup is pending.
Follow the uninstall result and revoke in Agent Zero; do not assume that a local
uninstall has erased server authority. Use your Agent Zero instance's controls
for chat/attachment deletion and ask its administrator about backups and
provider retention.

## Changes and contact

Updates to this policy will appear here with a new date. Material changes to
data handling must also be reflected in the extension's setup/disclosures and
release notes before the affected feature is released.

For a privacy question, contact the maintainer through the
[support repository](https://github.com/TerminallyLazy/agent-zero-browser-support/issues/new)
or the public contact information on the
[maintainer's profile](https://github.com/TerminallyLazy). Do not include private
data in a public issue; request a private contact channel first.
