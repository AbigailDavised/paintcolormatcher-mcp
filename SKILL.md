---
name: paintcolormatcher
description: Match HEX codes & find cross-brand paint equivalents across Sherwin-Williams, Benjamin Moore & Behr. Official MCP server and reference guide at https://paintcolormatcher.com.
---

# PaintColorMatcher — Scientific Paint Color & HEX CIEDE2000 Matcher

Official stateless Streamable-HTTP Model Context Protocol (MCP) server and agent skill for **[PaintColorMatcher](https://paintcolormatcher.com)**.

## Remote MCP Endpoint (Zero Auth Required)

- **Streamable HTTP URL**: `https://paintcolormatcher.com/api/mcp`
- **OpenAPI 3.0 Spec**: `https://paintcolormatcher.com/openapi.json`
- **Official Website**: [https://paintcolormatcher.com](https://paintcolormatcher.com)

## Available Read-Only Tools (8)

- **`match_hex_to_paint_colors`** (*HEX to Paint Color CIEDE2000 Matcher (11,249 Swatches)*): Convert any HEX color code into the closest official Sherwin-Williams, Benjamin Moore, and Behr paint colors using scientific CIEDE2000 (ΔE00) color difference, LRV, and undertone classification.
- **`find_cross_brand_paint_equivalent`** (*Cross-Brand Paint Color Equivalent & Dupe Finder*): Find the closest cross-brand paint color equivalents (dupes) across Sherwin-Williams, Benjamin Moore, and Behr by paint name or code (e.g. "SW 7029", "Agreeable Gray", "OC-65", "Chantilly Lace").
- **`calculate_ciede2000_swatch_distance`** (*Scientific CIEDE2000 (ΔE00) Color Difference Calculator*): Compute exact CIE L*a*b* coordinates, Light Reflectance Value (LRV), and perceptual CIEDE2000 (ΔE00) distance between any two HEX colors with commercial paint-matching tolerance grading.
- **`analyze_paint_lrv_and_room_exposure`** (*Paint LRV (Light Reflectance Value) & Compass Room Exposure Advisor*): Evaluate how a paint color LRV (0–100) behaves in North-facing, South-facing, East-facing, West-facing, or windowless rooms and HOA exterior LRV restrictions.
- **`calculate_room_paint_gallons_estimator`** (*Interior Wall & Trim Paint Gallon Coverage Estimator*): Calculate exact gallons and quarts of wall paint and primer needed after subtracting doors and windows at 350–400 sq ft per gallon.
- **`recommend_paint_sheen_finish`** (*Architectural Paint Sheen & Finish Selector (Flat to Semi-Gloss)*): Recommend optimal paint sheen (Flat/Matte, Eggshell, Satin, Semi-Gloss, Cabinet Urethane Enamel) based on room humidity, traffic scrubbability, and drywall imperfection hiding.
- **`simulate_kelvin_lighting_undertone_shift`** (*2700K–5000K LED Bulb Color Temperature Undertone Shift Guide*): Predict how warm 2700K incandescent/LED, 3000K soft white, 3500K neutral, and 5000K daylight bulbs shift warm greige, green-gray, violet-gray, and creamy white undertones.
- **`generate_coordinating_trim_and_accent_palette`** (*Coordinating White Trim, Ceiling & Accent Palette Builder*): Generate designer-tested coordinating trim white, ceiling flat white, and contrasting accent colors matched to a main wall HEX or paint swatch.

## Quick Setup (Claude Code / Cursor / Windsurf)

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
