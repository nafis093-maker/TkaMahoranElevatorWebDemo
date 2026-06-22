# Energy King — Concept Directions (Web Demo)

A single web app that showcases **three design directions** for the Energy King
elevator & smart-board website, so the client can compare them side by side and
pick one to build out.

Energy King represents elevators from **TKE, Marohn, Sharp, Hanjin and Movilift**,
and **ikinor** smart interactive boards.

## What's inside

```
TkaMahoranElevatorWebDemo/
├── index.html        ← the picker/viewer app (start here)
├── premium.html      ← Direction B · charcoal + champagne gold, serif, ascent beam
├── cinematic.html    ← Direction D · blue-black + amber, animated skyline, video-ready hero
├── kinetic.html      ← Direction E · charcoal + blueprint cyan, live shaft simulation
└── README.md
```

`index.html` frames each prototype in a switcher with desktop / tablet / mobile
preview widths and an "open full page" link. Keyboard shortcuts: **1 / 2 / 3**.

## Run locally

Just open `index.html` in a browser. (If a browser blocks the embedded previews
on `file://`, run a tiny local server instead:)

```bash
# from inside the project folder
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploy free on GitHub Pages

1. Push this repo to GitHub (see below).
2. On GitHub: **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**, Save.
4. Your live demo appears at
   `https://nafis093-maker.github.io/TkaMahoranElevatorWebDemo/` in a minute or two.

## Push to your repo

This folder is already a git repository with one commit. To publish it:

```bash
cd TkaMahoranElevatorWebDemo
git remote add origin https://github.com/nafis093-maker/TkaMahoranElevatorWebDemo.git
git branch -M main
git push -u origin main
```

If the remote already has commits and the push is rejected, either start clean
(`git push -u origin main --force`, only if you're sure the repo is meant to be
overwritten) or pull first (`git pull origin main --allow-unrelated-histories`)
and resolve, then push.

## Notes for the real build

- **Sample imagery** in the project tiles and the smart-board screen is original
  vector illustration — placeholder art, swap in real photos before launch.
- **The inquiry form is a front-end demo.** Submitting shows the auto-response
  ("Thank you for contacting Energy King…") but does not send mail yet. The real
  forward-to `sales@energyking.com` + auto-reply is a small backend (e.g. an
  ASP.NET Core endpoint or a form service) to wire up next.
- **Background video** in Cinematic / Kinetic: each hero has a `<video>` element
  ready for a real MP4 (marked with a comment) sitting over an animated canvas
  fallback. Drop in a short, compressed, muted loop with a poster image.
- Brand descriptions are placeholder copy — confirm positioning for TKE, Marohn,
  Sharp, Hanjin and Movilift before launch.

© 2026 Energy King — demo prepared for client selection.
