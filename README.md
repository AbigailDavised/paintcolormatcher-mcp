

[![mcptry](https://mcptry.com/badge/com.paintcolormatcher/mcp)](https://mcptry.com/servers/com.paintcolormatcher/mcp)
[![MCPRush Listing](https://mcprush.com/badge/paintcolormatcher-scientific-paint-color-hex-mcp/card.svg)](https://mcprush.com/to/paintcolormatcher-scientific-paint-color-hex-mcp?ref=badge)

[![Official Website](https://img.shields.io/badge/Website-paintcolormatcher.com-blue)](https://paintcolormatcher.com)
[![MCP Registry](https://img.shields.io/badge/MCP_Registry-com.paintcolormatcher%2Fmcp-green)](https://www.mcptry.com/servers/com.paintcolormatcher/mcp)
[![Glama Connector](https://img.shields.io/badge/Glama-Connector-purple)](https://glama.ai/mcp/connectors/com.paintcolormatcher/mcp)

Match HEX codes & find cross-brand paint equivalents across Sherwin-Williams, Benjamin Moore & Behr.

- **Official Workbench**: [https://paintcolormatcher.com](https://paintcolormatcher.com)
- **Remote MCP Endpoint**: `https://paintcolormatcher.com/api/mcp` (`streamable-http`, read-only, no API key required)
- **Public OpenAPI 3.0**: [https://paintcolormatcher.com/openapi.json](https://paintcolormatcher.com/openapi.json)
- **LLM Context**: [https://paintcolormatcher.com/llms.txt](https://paintcolormatcher.com/llms.txt) · [https://paintcolormatcher.com/llms-full.txt](https://paintcolormatcher.com/llms-full.txt)

## Tools Provided (8 Read-Only Tools)

| Tool Name | Summary |
| :--- | :--- |
| `match_hex_to_paint_colors` | Convert any HEX color code into the closest official Sherwin-Williams, Benjamin Moore, and Behr paint colors using scientific CIEDE2000 (ΔE00) color difference, LRV, and undertone classification. |
| `find_cross_brand_paint_equivalent` | Find the closest cross-brand paint color equivalents (dupes) across Sherwin-Williams, Benjamin Moore, and Behr by paint name or code (e.g. "SW 7029", "Agreeable Gray", "OC-65", "Chantilly Lace"). |
| `calculate_ciede2000_swatch_distance` | Compute exact CIE L*a*b* coordinates, Light Reflectance Value (LRV), and perceptual CIEDE2000 (ΔE00) distance between any two HEX colors with commercial paint-matching tolerance grading. |
| `analyze_paint_lrv_and_room_exposure` | Evaluate how a paint color LRV (0–100) behaves in North-facing, South-facing, East-facing, West-facing, or windowless rooms and HOA exterior LRV restrictions. |
| `calculate_room_paint_gallons_estimator` | Calculate exact gallons and quarts of wall paint and primer needed after subtracting doors and windows at 350–400 sq ft per gallon. |
| `recommend_paint_sheen_finish` | Recommend optimal paint sheen (Flat/Matte, Eggshell, Satin, Semi-Gloss, Cabinet Urethane Enamel) based on room humidity, traffic scrubbability, and drywall imperfection hiding. |
| `simulate_kelvin_lighting_undertone_shift` | Predict how warm 2700K incandescent/LED, 3000K soft white, 3500K neutral, and 5000K daylight bulbs shift warm greige, green-gray, violet-gray, and creamy white undertones. |
| `generate_coordinating_trim_and_accent_palette` | Generate designer-tested coordinating trim white, ceiling flat white, and contrasting accent colors matched to a main wall HEX or paint swatch. |

## Connect in 10 Seconds

### Claude Code
```bash
claude mcp add --transport http paintcolormatcher https://paintcolormatcher.com/api/mcp
```

### Cursor / Claude Desktop / Windsurf (`mcp.json`)
```json
{
  "mcpServers": {
    "paintcolormatcher": {
      "type": "streamable-http",
      "url": "https://paintcolormatcher.com/api/mcp"
    }
  }
}
```

### Agent Skill (`skills.sh`)
```bash
npx -y skills@latest add AbigailDavised/paintcolormatcher-mcp -y
```

## License

MIT © [PaintColorMatcher](https://paintcolormatcher.com)
