# Static Notes

![GitHub Repo Banner](https://ghrb.waren.build/banner?header=Static+Notes%F0%9F%97%92%EF%B8%8F&subheader=Single-file+note+sharing+app+with+URL-encoded+data&bg=14B8A6-06B6D4&color=FFFFFF&headerfont=Inter&subheaderfont=Kinewave&watermarkpos=bottom-right)
<!-- Created with GitHub Repo Banner by Waren Gonzaga: https://ghrb.waren.build -->

A single-file note sharing app that encodes your notes directly into the URL. No server, no database, no accounts — just share a link.

## How It Works

1. Write a note
2. The URL updates automatically with your encoded content
3. Copy and share the URL
4. Anyone who opens the link sees your note

That's it. Your note lives entirely in the URL.

## Features

- **URL-Encoded Storage** — Notes are compressed with lz-string and stored in the URL hash
- **No Backend** — Works entirely in the browser, even offline after first load
- **Rich Text** — Bold and italic formatting that survives the URL encoding
- **QR Code** — Generate a scannable QR code for easy mobile sharing
- **Dark Mode** — Automatically matches your system preference
- **Mobile Friendly** — Responsive design works on any device (320px+)
- **Keyboard Shortcuts** — Ctrl/Cmd + S (copy URL), L (clear), B (bold), I (italic)

## Usage

### Option 1: Open Directly
Download `index.html` and open it in your browser.

### Option 2: Deploy
Host `index.html` on any static hosting:
- GitHub Pages
- Netlify
- Vercel
- Any web server

It's a single file with no dependencies.

### Option 3: Use Online
If deployed, just visit the URL and start typing.

## URL Length Limits

URLs have practical limits:
- **< 2,000 chars** — Safe for all platforms
- **2,000 - 8,000 chars** — Works in most browsers, some apps may truncate
- **> 8,000 chars** — May hit browser limits

The app shows warnings as you approach these limits. For longer notes, use a URL shortener like Bitly or TinyURL — they preserve the full URL.

## Technical Details

- **Compression**: lz-string `compressToEncodedURIComponent()`
- **Editor**: Native `contenteditable` with `execCommand` for formatting
- **Encoding**: innerHTML preserved through compression (keeps `<b>`, `<i>` tags)
- **QR Code**: qrcode-generator library (inlined)
- **Size**: ~50KB total (HTML + CSS + JS, all inline)

## Browser Support

- Chrome 90+
- Firefox 90+
- Safari 14+
- Edge 90+
- Mobile Safari / Chrome

## License

MIT

## Credits

Built with [Claude Code](https://claude.ai/claude-code) using the Morgoth + Sauron SDLC workflow.
