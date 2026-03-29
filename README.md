# Album Rater Web

Responsive web app to search albums, rate tracks, manage pending listens, and use it from mobile or desktop.

## Includes

- Responsive UI for mobile and desktop
- Search albums by:
  - Spotify (server-side, optional)
  - Apple Music (server-side, optional)
  - MusicBrainz (works without credentials)
  - Manual album creation
- Track-by-track ratings:
  - 0.0 Worst
  - 0.25 Dislike
  - 0.5 Meh
  - 1.0 Like
  - 1.5 Love
- Final album score:
  - `score = 0.5 + 4.5 × (obtained / max)`
  - rounded to the nearest 0.5
  - slight bonus for many Love tracks
  - slight penalty for many Meh tracks
- Pending albums list
- Dark / Light mode
- English / Spanish
- Local persistence with `localStorage`

## Important note about APIs

For a web app, Spotify and Apple Music secrets must not be exposed in the browser.

This project handles Spotify and Apple Music on the server side through a Next.js API route.

Set credentials in `.env.local` locally or in your deployment platform environment variables.

## Quick start

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:3000
```

## Environment

Copy `.env.example` to `.env.local` and fill what you want:

```env
SPOTIFY_CLIENT_ID=
SPOTIFY_CLIENT_SECRET=
APPLE_MUSIC_DEVELOPER_TOKEN=
APPLE_MUSIC_STOREFRONT=us
```

- If Spotify credentials are missing, Spotify results are skipped.
- If Apple Music token is missing, Apple Music results are skipped.
- MusicBrainz still works.

## Deploy so you do not need your PC on

Best option:
- push to GitHub
- deploy on Vercel

That way the app stays online even when your PC is off.

## Data storage

This version stores ratings and pending albums in the browser with `localStorage`.

That means:
- easy setup
- no database needed
- but data is local to that browser/device

If later you want sync between phone and PC, the next upgrade would be Supabase or Firebase.
"# AlbumRaterWeb" 
