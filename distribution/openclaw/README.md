# PaintColorMatcher MCP for OpenClaw

PaintColorMatcher connects OpenClaw agents to deterministic calculators, decision advisors, and compatibility probes via a remote Streamable-HTTP MCP server.

- Website: https://paintcolormatcher.com
- Remote MCP endpoint: https://paintcolormatcher.com/api/mcp
- Source: https://github.com/AbigailDavised/paintcolormatcher-mcp

The bundle declares a `streamable-http` MCP connection. After enabling it in OpenClaw, verify connectivity by invoking only the read-only `match_hex_to_paint_colors` tool.
