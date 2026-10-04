# Privacy Policy — Codex Usage HUD

Last updated: 2026-10-04

Codex Usage HUD is a local macOS utility. It does not contain an AI model, advertising SDK, analytics SDK, or telemetry service.

## Data processed locally

The app stores the following data on the user's Mac:

- Codex lifecycle event name
- Session, turn, and subagent identifiers supplied by Codex Hooks
- Event timestamps
- Current usage percentage returned by the locally running Codex app-server
- HUD preferences such as collapsed state, peak level, and launch-at-login choice

## Data the app does not collect

The app does not read or store:

- Prompt or response text
- Tool arguments or tool output
- Source files or project contents
- Passwords, API keys, login tokens, or payment information

## Network access

The HUD does not add its own network client or send data to the developer or any third party. To read Codex usage limits, it starts the user's existing Codex executable locally. Any authentication or network communication performed by that executable is governed by the user's OpenAI/Codex configuration and OpenAI's applicable terms and privacy policy.

## Local storage

Runtime data is stored under:

`~/Library/Application Support/UsageHUD`

Users can remove this folder after disconnecting Codex Hooks and quitting the app.

## Contact

Developer contact information must be added before public distribution.
