---
name: roblox-studio-workflow
description: Use when the user wants to inspect, build, debug, or test a Roblox experience through the local Roblox Studio MCP connection.
---

# Roblox Studio workflow

1. Discover the actual available MCP tools. Call list_roblox_studios first and use the returned studio_id. If the target experience is ambiguous, ask the user to select it before making changes.
2. Call get_studio_state before selecting Edit, Client, or Server. Respect the current mode; switch modes only when needed for the authorized task.
3. Inspect the relevant scene and scripts before editing. Keep changes within the requested scope. Do not overwrite unrelated work or publish an experience without authorization.
4. Use small cohesive Luau modules and services, explicit dependencies, and composition for business workflows. Keep gameplay rules separate from persistence, platform services, and UI where useful. Avoid needless wrapper classes.
5. Retrieve relevant Roblox-provided skills using the server's skill tool when available. Use current official documentation for uncertain APIs. Do not invent tool names, schemas, or asset identifiers.
6. Verify the changed behavior with appropriate read-only inspection or an authorized playtest. Use screenshots for visual changes when available. Do not claim that static inspection proves runtime behavior.
7. Report what changed, what was verified, and any remaining limitation. If Studio is disconnected, ask the user to open the intended experience and enable its MCP server.

## Local connection

This Windows-only plugin runs Roblox's existing %LOCALAPPDATA%\Roblox\mcp.bat through cmd.exe. It does not distribute Roblox executables or provide a cloud server. Keep stdout reserved for the MCP protocol. If the same Roblox_Studio MCP server is configured globally, use one active connection to avoid duplicate tool listings.
