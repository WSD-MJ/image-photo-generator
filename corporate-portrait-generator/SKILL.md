---
name: corporate-portrait-generator
description: >
  Generate a polished, professional corporate portrait / business headshot from a
  personal photo. Upload a selfie and get a clean, high-end business portrait with
  selectable backgrounds and outfit styles — no influencer glamour, just a reliable
  professional look. Use when the user wants an AI headshot, corporate portrait,
  business headshot, LinkedIn photo, professional profile photo, 职业照 / 商务形象照 /
  职场头像, or a team of uniform staff portraits. Trigger keywords: headshot, AI
  headshot, corporate portrait, business photo, professional avatar, LinkedIn photo,
  职业照, 商务照, 形象照, 职场头像. Requires an API key from wsdsocial.com.
---

# Corporate Portrait Generator

Generate professional corporate portraits / business headshots with AI. Upload a
personal photo and choose from multiple background and outfit styles to get a clean,
polished, business-grade portrait.

## Setup

1. Get your API key at https://ai.wsdsocial.com/skills
2. Set as environment variable: `WSD_API_KEY`

## Usage

```bash
curl -X POST "https://ai.wsdsocial.com/api/pub/skills/corporate-portrait-generator/_tool_90" \
  -H "Content-Type: application/json" \
  -H "key: ${WSD_API_KEY}" \
  -d '{
    "request": "Classic light gray background, executive suit",
    "custom_data": {
      "files": ["https://example.com/photo.jpg"]
    }
  }'
```

## Parameters

| Param               | Type          | Required | Description |
|---------------------|---------------|:--------:|-------------|
| `request`           | String        | Yes      | Styling preferences. Background options: classic light gray, seamless pure white. Outfit options: executive suit, business shirt, corporate polo. Designed for formal use cases such as employee badges, staff ID cards, access cards, and company team pages. |
| `custom_data`       | Object        | No       | Photo data container |
| `custom_data.files` | Array<String> | No       | List of photo URLs or base64-encoded images |

## Response

Returns the generated corporate portrait image URL.
