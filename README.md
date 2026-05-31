# Crate — Music Collection Manager

A clean, minimal web app to catalogue your music collection. Add, browse, and manage vinyl records, CDs, and cassettes — with cover art, full metadata, and import/export support.

**[Live demo →](https://YOUR-USERNAME.github.io/crate/)**

---

## Features

- **Browse your collection** — grid and list views, search by artist/title/label, filter by format
- **Add & edit records** — artist, title, label, format, year, notes, and cover image upload
- **Formats supported** — 12" vinyl, 7" vinyl, CD, cassette
- **User authentication** — sign in / register with username and password
- **User management** — admin role can add, delete, and promote/demote users
- **Import / Export** — JSON (full fidelity, includes images) and CSV (for spreadsheets)
- **Dark mode** — respects your system preference
- **Responsive** — works on desktop and mobile

---

## Getting started

### Option 1 — Open locally

Download `index.html` and open it in any modern browser. No install, no server needed.

### Option 2 — GitHub Pages (recommended)

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set branch to `main`, folder to `/root`, and save
4. Your app will be live at `https://YOUR-USERNAME.github.io/crate/`

---

## Default login

| Username | Password | Role  |
|----------|----------|-------|
| `admin`  | `admin`  | Admin |

**Change the admin password after your first login** via User management → delete the default user and create a new one.

---

## Data storage

All data is stored in your browser's `localStorage`. This means:

- Data persists across page refreshes and browser restarts
- Data is local to the device and browser you use
- Clearing browser data will erase your collection — **export regularly as a backup**

To move your collection to another device or browser, use **Import / Export → Export JSON**, then import the file on the new device.

---

## CSV import format

The CSV must include a header row. Column order doesn't matter.

| Column   | Required | Notes                                         |
|----------|----------|-----------------------------------------------|
| `artist` | Yes      |                                               |
| `title`  | Yes      |                                               |
| `label`  | No       |                                               |
| `format` | No       | `12-inch`, `7-inch`, `CD`, or `Cassette`      |
| `year`   | No       | Four-digit year                               |
| `notes`  | No       | Condition, pressing info, personal notes, etc.|

Example:

```csv
artist,title,label,format,year,notes
Massive Attack,Mezzanine,Virgin,12-inch,1998,Original UK press
Portishead,Dummy,Go! Beat,CD,1994,
The Cure,Boys Don't Cry,Fiction,7-inch,1979,Near mint
```

---

## Tech stack

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build step, no dependencies except the [Tabler Icons](https://tabler.io/icons) webfont for icons.

---

## License

MIT
