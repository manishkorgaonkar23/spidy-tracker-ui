# 🕷️ Spidy Tracker

A retro, pixel-art styled live location-sharing web app — track and share real-time "spider sightings" on an interactive map.

**Live site:** [manishkorgaonkar23.github.io/spidy-tracker-ui](https://manishkorgaonkar23.github.io/spidy-tracker-ui/)

## Features

- 📍 **Track Now** — share your live GPS location as a "sighting" on the map
- 🗺️ **2D Map** — interactive Leaflet.js map with dark/light theme
- 🌐 **3D Globe** — toggle to a rotating 3D globe view of all sightings
- 🕸️ **Spider Sense** — radar that highlights sightings near your location
- 🟢 **Live visitor counter** — see how many people are on the site right now
- 🔊 Sound effects and voice alerts
- 📤 Share your location link with others

## Tech Stack

- **Frontend:** HTML, CSS, vanilla JavaScript
- **Map:** [Leaflet.js](https://leafletjs.com/) (2D) + [Globe.gl](https://globe.gl/) (3D, lazy-loaded)
- **Backend / Database:** [Supabase](https://supabase.com/) (Postgres + Realtime + Row Level Security)
- **Hosting:** GitHub Pages

## How it works

1. Open the site and tap **Track Now**
2. Your device's GPS location is saved as a sighting via Supabase
3. Everyone currently viewing the site sees your pin appear live, in real time
4. Re-tapping **Track Now** updates *your* pin instead of creating a new one

## Notes

- The Supabase URL and publishable (anon) key in the code are meant to be public — this is standard practice for client-side apps. Actual data access is controlled by Supabase **Row Level Security (RLS)** policies, not by hiding the key.
- Sightings older than 30 days are automatically hidden from the map to keep it clutter-free.

---

Built and maintained by [@manishkorgaonkar23](https://github.com/manishkorgaonkar23)
