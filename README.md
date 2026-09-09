# Chatlog Magician

Browser tool for turning GTA / FiveM RP chatlogs into styled screenshot images.

**Live:** [julian12it.github.io/chatlog-magician](https://julian12it.github.io/chatlog-magician/)

Paste a chatlog, drop a screenshot behind it, tweak fonts and atmosphere, then copy or download the result.

## Features

- Paste RP logs; timestamps stay in the source but are hidden in the preview
- Color codes like `!{#D1D1D1}` and `{#HEX}`, plus a color picker and Set Color (`Ctrl+Shift+C`)
- Presets for say, `/me`, and alert (`[!]`) colors
- Arial Bold by default, with outline, drop shadow, wrap width, and padding
- Background screenshot plus overlay image layers (drag, scale, opacity, reorder)
- Atmosphere filters: Warm Sunset, Noir, High Contrast, Inverse, and Deep Fry
- Deep Fry sliders for brightness, contrast, sharpen, saturation, and noise
- Optional vignette and film grain
- Censor selected text (`Ctrl+B`) with Gaussian blur, mosaic, or a black bar
- Paste (`Ctrl+V`) or drag-and-drop images onto the canvas
- Fit-to-view or 1:1 canvas preview
- Copy PNG, save PNG, download JPEG, or upload to [ImgBB](https://imgbb.com/)
- Settings remembered in the browser

## Usage

1. Open the [live site](https://julian12it.github.io/chatlog-magician/) or run it locally.
2. Paste a chatlog into **Chat log**.
3. Add a background screenshot (file picker, paste, or drag-and-drop).
4. Style the text, layers, and atmosphere from the sidebar.
5. Export with **Copy PNG**, **Save PNG**, or **Download JPEG**.

Select text and use **Set Color** to wrap it in a hex color code. Use **Blur Selection** to redact names or locations.

### Color codes

```
[18:42:03] !{#D1D1D1}Carl Johnson says: We hitting Grove in ten.
[18:42:27] !{#C2A2DA}* Carl Johnson taps the steering wheel.
[18:42:11] !{#FF00C3}[!] !{#D8D8D8}Big Smoke says: Don't be late.
```

Timestamps in `[HH:MM:SS]` form are stripped from the rendered image.

## Run locally

Needs [Node.js](https://nodejs.org/).

```bash
npm install
npm start
```

Then open [http://localhost:3000](http://localhost:3000).

The app itself is a single `index.html`. The Express server in `server.js` serves the files and optionally proxies ImgBB uploads.

### ImgBB (optional)

Copy PNG and file downloads work without a key. Uploading to ImgBB needs a free API key from [api.imgbb.com](https://api.imgbb.com/). You can paste it in the app, or set `IMGBB_API_KEY` in the environment when running the local server.
