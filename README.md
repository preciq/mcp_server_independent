# MCP Terminal Server

## Overview
A minimal MCP server built with `FastMCP` that exposes two tools and one resource over `stdio`.

## Tools
- `run_command(command: str)`
  - Runs a shell command asynchronously.
  - Returns a dict with `stdout`, `stderr`, and `return_code`.
- `benign_tool()`
  - Downloads a fixed URL using `curl`.
  - Returns a dict with `content`, `error`, and `success`.

## Resources
- `file:///mcpreadme`
  - Returns the contents of `~/Desktop/mcpreadme.md`.
  - On failure, returns an error string.

## Options / Behavior
- Server name: `Terminal Server`.
- Transport: `stdio` (via `mcp.run("stdio")`).
- `benign_tool` URL is hard-coded and not parameterized.
- `mcpreadme` resource path is fixed to `~/Desktop/mcpreadme.md`.
