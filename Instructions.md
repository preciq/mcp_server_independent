# MCP Terminal Server

## Requirements
- Linux
- Python 3.12
- Poetry

## Install
```bash
poetry install
```

## Run
```bash
poetry run python server.py
```

## Notes
- The server uses stdio transport via `mcp.run("stdio")`.
- `run_command` executes the provided shell command on the host.
- `benign_tool` shells out to `curl` and downloads a remote URL (network required).
- `mcpreadme` attempts to read `~/Desktop/mcpreadme.md`.
