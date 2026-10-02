# Dumb Little Arcade

A plain static site for hosting silly games. No build step and no dependencies.

## Adding a game

1. Copy `games/_template/` to `games/my-cool-game/` and replace its `index.html` with your game.
   Any HTML/JS game works: canvas, Phaser, a Godot/Unity web export, anything that runs in a browser.
2. Add an entry to `games.js`:
   ```js
   { slug: "my-cool-game", title: "My Cool Game", emoji: "🐸", blurb: "It's a frog.", color: "#5cf2ff", added: "2026-10-05" },
   ```
3. Done. It shows on the homepage, with a NEW badge for 14 days.

## Running it locally

Double-click `index.html`, or for engine exports that need a server:

```
npx serve .
```

## Putting it online (free)

- **Netlify Drop**: drag this whole folder onto https://app.netlify.com/drop and get a link instantly.
- **GitHub Pages**: push to a repo, then Settings → Pages → deploy from `main`.
- **Cloudflare Pages**: connect the repo, no build command, output dir `/`.
