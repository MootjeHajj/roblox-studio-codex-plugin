# Roblox Studio for Codex

A Windows-local Codex plugin connecting to the Roblox Studio MCP server already installed on the user's computer. It provides a reusable workflow for inspecting scenes and Luau scripts, making scoped changes, and verifying behavior.

## Requirements

- Windows, Codex with local plugin support, and Roblox Studio with MCP support.
- The existing \%LOCALAPPDATA%\Roblox\mcp.bat launcher must be present.
- Open the intended experience in Studio and enable its MCP server.

## Install from this public source marketplace

Register this GitHub repository through Codex's supported plugin marketplace flow, then install roblox-studio from roblox-community. Check your installed Codex version's plugin help for available commands. The repository includes .agents/plugins/marketplace.json and the plugin under roblox-studio/.

Example prompts: “Inspect my Roblox project and explain its structure”; “Help me debug this Luau script after inspecting the current Studio state.”

## Scope and security

The package launches Roblox's existing server through cmd.exe. It includes no Roblox executables, credential files, remote server, public tunnel, or gameplay assets. Studio edits and playtests remain subject to the user's requested scope. Use one active MCP configuration to avoid duplicate tools.

This is a local Codex source marketplace package. Public GitHub distribution does not provide a ChatGPT web/mobile connection and is not approval in the public OpenAI plugin directory or the Roblox Creator Store. Uploading a package does not deploy or authenticate its server.

## Verification

Release packaging checks inspect the JSON manifests, matching skill identity, contained references, archive inventory, personal paths, and secret patterns. A fresh installation and live Studio behavior have not been tested for this release; do not treat package validation as runtime verification.

## Attribution

The package metadata identifies Moham as its original author. Roblox Studio and its MCP implementation belong to their respective owners. This independent integration is not affiliated with or endorsed by Roblox. No new license grant is asserted by this release.
