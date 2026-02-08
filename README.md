# Pollinations.ai Image Model Comparison Tool

[![Built with Pollinations](https://img.shields.io/badge/Built%20with-Pollinations-8a2be2?style=for-the-badge&logo=data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%20124%20124%22%3E%3Ccircle%20cx%3D%2262%22%20cy%3D%2262%22%20r%3D%2262%22%20fill%3D%22%23ffffff%22%2F%3E%3C%2Fsvg%3E&logoColor=white&labelColor=6a0dad)](https://pollinations.ai)

A web-based tool for comparing AI image generation models side-by-side using the [Pollinations.ai](https://pollinations.ai) API.

![Pollinations.ai Logo](https://raw.githubusercontent.com/pollinations/pollinations/main/assets/logo-text.svg)

## Features

- **Model Comparison**: Compare multiple AI image models simultaneously
- **BYOP Integration**: Connect your Pollinations account (Bring Your Own Pollen) or use the free tier
- **Smart Rate Limiting**: Automatic retry with countdown timers (3 attempts max)
- **Scene & Style Prompts**: Autocomplete input fields with 10 preset scenes and 10 preset styles
- **Sequential Processing**: Queue system to respect API rate limits
- **Real-time Status**: Visual feedback for pending, loading, waiting, success, and error states
- **Mobile Responsive**: Works on desktop and mobile devices

## Quick Start

1. Open `image-comparison/index.html` in your browser
2. Select a **Scene** and **Style** from the autocomplete fields (or type your own)
3. Choose which models to test using the model tags
4. Click **Test All Models** to start generating images
5. View results side-by-side with timing and cost information

## BYOP (Bring Your Own Pollen)

Connect your Pollinations account to use your own API credits:

1. Click **Connect with Pollinations**
2. Authorize the app at `enter.pollinations.ai`
3. You'll be redirected back with your API key stored locally
4. Your account tier and balance will be displayed

If rate limited on your account, the tool automatically falls back to the free tier.

## Rate Limiting

The tool handles rate limits gracefully:
- **Sequential requests**: Models are tested one at a time with delays
- **Automatic retry**: Up to 3 retry attempts per model
- **Countdown timers**: Shows time remaining before retry
- **Smart fallback**: BYOP users fall back to free tier when rate limited
- **Cancel option**: Stop all pending retries at any time

## Available Models

Models are fetched dynamically from the Pollinations API. Popular models include:
- `flux` - High-quality general purpose
- `gptimage` - OpenAI's image model
- `zimage` - Optimized for speed
- `nanobanana` - Alternative architecture

## File Structure

```
pollinations/
├── image-comparison/
│   └── index.html          # Main application file
└── README.md               # This file
```

## Technology

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **API**: [Pollinations.ai Image Generation API](https://pollinations.ai)
- **Authentication**: OAuth2 via `enter.pollinations.ai`
- **Storage**: LocalStorage for API key persistence

## Configuration

The tool works out of the box with no configuration required. Optional settings:

- **API Key**: Stored in browser LocalStorage (30-day expiry)
- **Auto-test**: Add `?autotest` to URL for automatic testing on load

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## SEO & Sharing

The page includes comprehensive meta tags for:
- Search engine optimization (SEO)
- Open Graph (Facebook sharing)
- Twitter Cards
- Favicon and brand assets

## Credits

- Built with [Pollinations.ai](https://pollinations.ai)
- Logo and brand assets from [Pollinations GitHub](https://github.com/pollinations/pollinations)

## Links

- 🌐 [pollinations.ai](https://pollinations.ai)
- 📖 [API Documentation](https://pollinations.ai)
- 🎨 [Logo White](https://raw.githubusercontent.com/pollinations/pollinations/main/assets/logo.svg)
- 🎨 [Logo Text White](https://raw.githubusercontent.com/pollinations/pollinations/main/assets/logo-text.svg)

## License

This project is open source and available under the MIT License.

---

**Powered by [Pollinations.ai](https://pollinations.ai)** - Free AI Image Generation API
