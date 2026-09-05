# Sample match output

A complete rendered pipeline output. Open `match_report.html` in a browser for
the dashboard view.

## Which of these files are synthetic

Heart-rate derived values are generated, not measured, and the roster uses real
footballers' names as recognisable placeholders. No real athlete was recorded.

| File | Status |
| --- | --- |
| `physio.json` | Synthetic — tagged `data_classification: "SYNTHETIC"` |
| `player_identities.json` | Synthetic names — tagged in-band |
| `shots.json` | Synthetic attribution — tagged in-band |
| `physio_timeline.csv` | Synthetic — schema left untouched, see this table |
| `players_summary.csv` | `mean_hr_bpm`, `max_hr_bpm`, `trimp` synthetic; distance and speed columns are vision-derived |
| `shots.csv` | Ballistics vision-derived; `player_name` synthetic |
| `match_report.html` | Renders a synthetic-data banner at the top |
| `homography.json` | Real measurement |
| `metrics_summary.json` | Real measurement |
| `team_assignment.json` | Real measurement |

The CSV files carry no in-band tag because adding a column would misrepresent
the export schema a coach actually receives. They are documented here instead.

Full detail: [`../../docs/DATA_DISCLAIMER.md`](../../docs/DATA_DISCLAIMER.md)
