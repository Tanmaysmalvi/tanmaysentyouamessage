# Girlfriend's Day 💖

A one-page surprise: it asks *"Hey babe… do you love me?"* — the **Yes** button keeps growing, and the **No** button runs away every time she gets close to it.

Everything lives in a single `index.html` file. No build step, no dependencies, works offline (fonts fall back gracefully).

## Try it

Double-click `index.html`, or from this folder:

```bash
open index.html
```

## Make it personal

Open `index.html` and edit the `CONFIG` block near the top of the `<script>` tag:

| Field | What it does |
| --- | --- |
| `herName` | Shown in the question and in the reveal ("I love you too ___") |
| `question` | The question itself |
| `message` | Your custom message after she clicks Yes. Use `\n\n` for a new paragraph |
| `signoff` | The handwritten line at the bottom |
| `photoUrl` | Optional photo of you two. Set it to `"us.jpg"` and drop that file next to `index.html` |
| `noLabels` | Text the No button cycles through as it escapes |
| `taunts` | The line under the question, one per dodge |

## How the No button behaves

- On desktop it dodges as soon as the cursor gets within ~70px, so it's never actually clickable.
- On phones there's no hover, so it jumps on tap instead — same effect.
- It stays inside the screen, avoids landing on top of the Yes button, and shrinks a little each time while Yes grows.

## Send it to her

Any static host works since it's one file:

- **Netlify Drop** — drag this folder onto [app.netlify.com/drop](https://app.netlify.com/drop), get a link instantly.
- **GitHub Pages** — push the folder, enable Pages on the `main` branch.
- **Vercel** — `npx vercel` in this folder.

Or just AirDrop / WhatsApp the `index.html` file and let her open it.
