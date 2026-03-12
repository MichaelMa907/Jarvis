# Learned Instructions
created: 2026-03-12
last_reviewed: 2026-03-12

## MCP And Tools
- [active] mcp_discovery: check available MCP tools before refusing a task that seems impossible, especially Zapier for connected user apps | trigger=task seems unsupported or impossible | source=mistake | first_learned=2026-03-11 | last_updated=2026-03-12
- [active] browser_viewing: use the Playwright MCP for tasks that require browser viewing or interaction | trigger=web pages need to be viewed or manipulated | source=convention | first_learned=2026-03-12 | last_updated=2026-03-12

## Outlook
- [active] outlook_standard_actions: prefer standard Zapier Outlook actions before `microsoft_outlook_api_request_beta` when the standard action already supports the operation | trigger=Outlook calendar tasks via Zapier | source=mistake | first_learned=2026-03-11 | last_updated=2026-03-12
- [active] outlook_reminder_minutes: explicitly pass `reminderMinutesBeforeStart` instead of only setting `isReminderOn` when creating Outlook events with reminders | trigger=Outlook event creation with reminder requirements | source=mistake | first_learned=2026-03-11 | last_updated=2026-03-12
- [active] outlook_beta_fallback: only use `microsoft_outlook_api_request_beta` when the standard Outlook action cannot express the needed field or operation | trigger=standard Outlook action appears limited | source=mistake | first_learned=2026-03-11 | last_updated=2026-03-12

## Cloudflare Tunnel
- [active] tunnel_handoff: do not hand off a `trycloudflare.com` URL until `cloudflared` is still running after the launching shell exits | trigger=sharing a temporary Cloudflare Tunnel URL | source=migration | first_learned=2026-03-12 | last_updated=2026-03-12
- [active] tunnel_verification: verify local origin response, running `cloudflared` process, tunnel log registration, and public URL response before reporting a tunnel as ready | trigger=validating a Cloudflare tunnel | source=migration | first_learned=2026-03-12 | last_updated=2026-03-12
- [active] tunnel_launch_mode: prefer launching `cloudflared` detached with `setsid ... </dev/null >... 2>&1 &` and writing a pid file | trigger=starting a tunnel intended to outlive the launching shell | source=migration | first_learned=2026-03-12 | last_updated=2026-03-12
- [active] tunnel_error_1033: treat Cloudflare `Error 1033` as evidence that the hostname exists but no active tunnel connector is behind it | trigger=Cloudflare Tunnel error 1033 | source=migration | first_learned=2026-03-12 | last_updated=2026-03-12

## Codex Sessions
- [active] codex_resume_uuid: when sharing a resumable Codex session, use the conversation/session UUID, not the temporary `exec_command` or `write_stdin` session id | trigger=user asks for a Codex session id for `codex resume` | source=mistake | first_learned=2026-03-12 | last_updated=2026-03-12

## Recovery Snapshot
- [active] snapshot_scope: keep `/home/opc/Jarvis` as a sanitized root-style recovery snapshot containing only durable files needed to recreate the Codex environment; exclude secrets, auth state, caches, editor/tool state, `mcserver`, temp archives, and packaging directories | trigger=updating the persistent recovery repo | source=mistake | first_learned=2026-03-12 | last_updated=2026-03-12

## Notes
- Keep this file focused on reusable lessons, not user profile memory.
