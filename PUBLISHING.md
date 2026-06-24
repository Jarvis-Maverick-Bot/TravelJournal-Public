# Publishing Policy

## Manual Gate

First-cohort publishing is manual-gated.

Required publish signal:

```text
PUBLISH_FIRST_COHORT_STATIC
```

The D36 first-cohort package was published after Alex provided this signal on 2026-06-24.

Future day packages still require the same explicit publish signal unless the daily cron publish gate is separately enabled.

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
