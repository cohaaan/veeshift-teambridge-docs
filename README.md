# Teambridge Docs (VeeShift)

Searchable HTML documentation for:

1. **clone-blueprint.html** — build a new staffing clone from scratch
2. **veeshift-internal.html** — existing VeeShift Teambridge account (live schema + ops)

Open `index.html` in a browser.

## Regenerate schema JSON

Use OAuth client credentials from `teambridge-proxy-admin/.env` (not stored here) to call:

```
GET https://open-api.teambridge.com/v1/collections
GET https://open-api.teambridge.com/v1/collections/{id}/fields
```

Then refresh `data/collections-summary.json` and re-run the generator if present.

## Security

Do not commit API client secrets, webhook secrets, or database URLs into this repo.
