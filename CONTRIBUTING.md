# Contributing

The README is generated. Edit the data, then rebuild.

1. Add or change an entry in [`data/events.json`](data/events.json).
2. If you changed dates or deadlines, set `as_of` at the top of the file to today's date.
3. Run `python3 scripts/build.py` (Python 3.9+, no dependencies).
4. Commit both `data/events.json` and `README.md` and open a pull request.

## Entry fields

| Field | Required | Notes |
|---|---|---|
| `name`, `host`, `where`, `when` | yes | `when` is free text, e.g. `Feb 12–14, 2027` |
| `apply` | yes | How and by when to apply |
| `url` | yes | Official site, `https://` only |
| `source` | yes | `official`, `listing` or `pattern` (see below) |
| `start`, `deadline` | no | `YYYY-MM-DD`; drive the status column and the deadlines table |
| `size`, `perks`, `notes` | no | Attendance, prizes and travel, anything else |
| `category` | competitions only | Groups the competitions section |

## Which `source` to use

- `official`: you read the dates on the event's own site, the MLH season page, or its Devpost page.
- `listing`: the information comes from a third-party listing or job board.
- `pattern`: this cycle's dates are not posted; you are recording when it usually happens.

Do not mark something `official` from memory. If in doubt, use `pattern` and say what is uncertain in `notes`.

## What belongs here

- Collegiate hackathons with a few hundred or more attendees, or regional significance
- Company-run hackathons and programmes that students can apply to
- Competitions open to university students

Put a hackathon in `collegiate_36h` or `collegiate_24h` by its hacking period. If the site does not state the duration, say so in `notes`.
