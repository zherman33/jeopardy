# Christine's Bachelorette Jeopardy! 🥂

A custom Jeopardy-style web app built for Christine's bachelorette party weekend (June 12–14, 2026).

## Features

- **AI Board Builder** — Chat with the AI assistant to generate a fully custom Jeopardy board based on Christine, Andrew, and the group
- **Manual Mode** — Enter category names yourself and fill in questions directly
- **Live Board Config** — Edit any question or answer in real time before launching
- **Demo Mode** — A sample board is pre-loaded so you can preview the game immediately
- **QR Code Buzzer** — Players scan a QR code on their phones to join and buzz in
- **Score Tracking** — Automatic score management per player
- **Three Pages:**
  - `#setup` — Configure your board (AI or manual)
  - `#board` — The projected game board (host view)
  - `#player` — Mobile buzzer for players

## Setup & Deployment

### Option 1: GitHub Pages (Recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your app will be live at `https://yourusername.github.io/christine-jeopardy/`

### Option 2: Netlify (Drag & Drop)

1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag the entire folder onto the page
3. Done — you'll get a live URL instantly

### Option 3: Vercel

```bash
npx vercel
```

## Using the AI Board Builder

The AI assistant requires an **Anthropic API key** to generate boards. To use it:

1. Get an API key from [console.anthropic.com](https://console.anthropic.com)
2. The app calls the API directly from the browser — for a production deployment, consider setting up a small backend proxy to keep your key secure

If you don't have an API key, use **Manual Mode** to enter categories yourself, then fill in questions in the Board Config panel.

## How to Play

1. Open the app and chat with the AI (or use Manual mode) to build your board
2. Review and edit questions in the **Board Config** panel on the right
3. Click **Open Game Board** to launch the host view
4. Add players manually or have them scan the **QR code** with their phones
5. Players buzz in from their phones; the host reveals answers and awards points

## Tech Stack

- Vanilla HTML/CSS/JavaScript — no framework, no build step
- [QRCode.js](https://github.com/davidshimjs/qrcodejs) for QR generation
- Google Fonts: Bebas Neue, Playfair Display, Lato
- Anthropic API (`claude-sonnet-4-20250514`) for AI board generation
- `localStorage` for cross-device buzzer sync

## Customization

The demo board content, color palette, and fonts can all be changed directly in `index.html`:

- **Colors** — edit the CSS variables at the top of the `<style>` block (`:root { ... }`)
- **Demo board** — edit the `DEMO_BOARD` array in the `<script>` block
- **Fonts** — swap the Google Fonts link and update the CSS variables

---

Made with ✦ for Christine's Bachelorette Weekend
