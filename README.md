# Album Rater Web

Responsive web app to search albums, rate tracks, manage pending listens, and use it from mobile or desktop.

## Includes

- Responsive UI for mobile and desktop
- Search albums by:
  - Spotify (server-side, optional)
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

