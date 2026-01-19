# Gemini Configuration Example

Example configuration for using Google's Gemini API for image generation.

## Configuration

```yaml
# .claude/github-social.local.md
---
provider: gemini
api_key_env: GEMINI_API_KEY
output_path: .github/social-preview.png
dimensions: 1280x640
include_text: true
colors: auto
upload_to_repo: false
---
```

## Environment Setup

Set your Gemini API key:

```bash
export GEMINI_API_KEY="your-api-key-here"
```

Get your API key from [Google AI Studio](https://aistudio.google.com/).

## Models

| Model | Description | Best For |
|-------|-------------|----------|
| `gemini-2.5-flash-image` | Fast, efficient | High-volume, quick iterations |
| `gemini-3-pro-image-preview` | Higher quality with reasoning | Final production images, text rendering |

Default model is `gemini-2.5-flash-image` for speed.

## Cost

- **Gemini 2.5 Flash Image**: ~$0.039 per image (1290 output tokens at $30/1M tokens)
- Free tier available with rate limits

## Expected Behavior

When running `/social-preview`:

1. Project files are analyzed
2. Image prompt is generated
3. Gemini API is called with the prompt
4. Image is downloaded and saved to output path
5. File location and size are reported

## Troubleshooting

### API Key Not Found
Ensure `GEMINI_API_KEY` is set in your environment or configured in `api_key_env`.

### Rate Limiting
Free tier has usage limits. Consider upgrading or spacing out requests.

### Image Quality Issues
Try switching to `gemini-3-pro-image-preview` for higher quality output with better text rendering.

## API Request Format

The skill uses this API format:

```bash
curl -X POST \
  "https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-image:generateContent" \
  -H "x-goog-api-key: $GEMINI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "contents": [{"parts": [{"text": "Your prompt"}]}],
    "generationConfig": {
      "responseModalities": ["IMAGE"],
      "imageConfig": {"aspectRatio": "16:9"}
    }
  }'
```

## Comparison with Other Providers

| Feature | Gemini | DALL-E 3 | SVG |
|---------|--------|----------|-----|
| Cost | ~$0.039 | ~$0.08 | Free |
| Speed | 3-10s | 5-15s | Instant |
| Quality | Good | Artistic | Clean |
| Editability | No | No | Yes |
| Free Tier | Yes | No | N/A |

## Recommendation

Use Gemini when:
- You want AI-generated imagery at lower cost than DALL-E
- You have the free tier available
- You need faster generation than DALL-E
- SVG doesn't meet your visual needs

Consider SVG (default) for:
- Free, instant generation
- Clean, professional look
- Editable output
- Consistent results
