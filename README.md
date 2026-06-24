# DownMite live status

`status.json` here controls the "Service status" notices inside the DownMite app.
Edit it, commit, push → every app shows it on next launch.

## Post a message

Edit `status.json` (here on github.com → click the file → pencil icon → commit):

```json
{
  "notices": [
    {
      "title": "YouTube downloads delayed",
      "message": "YouTube changed something. A fix is in progress — thanks for your patience.",
      "level": "warning",
      "time": "Today"
    }
  ]
}
```

- **title** — short bold heading (required)
- **message** — body text users read (required)
- **level** — `info` (blue) · `warning` (amber) · `outage` (red). Default: `info`.
- **time** — optional label like `"Today"`. Cosmetic.

Add more `{ }` objects for multiple notices.

## Clear everything (back to "All systems normal")

```json
{ "notices": [] }
```
