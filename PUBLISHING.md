# Publishing Policy

## Manual Gate

Current first-cohort publishing is manual-gated.

Required publish signal:

```text
PUBLISH_FIRST_COHORT_STATIC
```

Until that signal is given, this public repository must keep the placeholder page and must not expose the generated D36 replay package.

## Allowed Content

- Static HTML, CSS, JSON, markdown, image, and audio files required for the approved preview.
- Feedback template for the approved cohort.
- Minimal metadata needed by the static replay page.

## Disallowed Content

- Private TravelJournal source history.
- Routine local daily output.
- `state.json` from the private generation workspace.
- Credentials, local absolute paths, `.env` files, cache files, or unreviewed generated media.

## Later Cron Sync

When stable, the daily cron may sync into this repository only after:

1. Daily generation completes.
2. Required images and narration audio exist.
3. Static replay smoke checks pass.
4. Secret/path scans pass.
5. The publish gate is enabled for that day.
