# Backup Tracker

A web-based daily backup recording and statistics tool. Built with vanilla HTML/CSS/JS — no build step, no framework, no backend. Data is stored entirely in your browser via localStorage.

[**简体中文**](README.zh-CN.md)

## Features

- **Daily Entry** — Log backup jobs with system, type, status, data size, duration, operator, source path, media, volume label/SN, and notes
- **Data Locking** — Lock individual records or lock all visible records to prevent accidental edits or deletions
- **Statistics & Charts** — Success rate trends, daily distribution bar chart, system-wise success rate, and status distribution pie chart (powered by ECharts)
- **History Filtering** — Filter records by date range, system, and status
- **Excel Import** — Import records from `.xls` / `.xlsx` files with automatic header detection
- **Excel Template Download** — Generate a blank template for offline data collection
- **Cloud Sync** — Sync data across browsers via GitHub API. Configure a Personal Access Token in Management → Cloud Sync, and data auto-pushes to the repository on every save.
- **Dark Sci-Fi UI** — Particle animation background, glow effects, scanline overlay

## Usage

1. Open `index.html` in a browser (or visit the [live site](https://tsuimanlung.github.io/backup_tracker/))
2. Fill in the backup details and click **Save**
3. Switch to **History** tab to view, filter, lock, or delete records
4. Switch to **Statistics** tab for visual analysis
5. Go to **Management** → **Cloud Sync** to configure GitHub sync for cross-browser data sharing

All data is persisted in your browser's localStorage and optionally synced to your GitHub repository.

## Data Fields

| Field | Description |
|---|---|
| Date | Backup execution date |
| System | Backup system (12 predefined options) |
| Type | Full / Incremental / Differential / Snapshot |
| Status | Success / Fail / Partial / In Progress |
| Data Size | e.g. `256.3 GB` |
| Duration | e.g. `1h 23m` |
| Operator | Person who performed the backup |
| Source Path | Backup source (default: `D:\ACH Shared`) |
| Media | External HDD / NAS / Tape Drive / Object Storage / Optical Disc / Other |
| Volume Label | My Book 1 / My Passport / 2020-My Book |
| Volume SN | 70C4-4CBE / 56C3-C608 / 020E-E18E |
| Note | Free-text notes |

## Tech Stack

- [ECharts](https://echarts.apache.org/) — charting library
- [SheetJS (xlsx)](https://sheetjs.com/) — Excel import and template generation
- localStorage — data persistence

## License

MIT
