# D36 UAT Readiness

This package is a UAT readiness candidate only. It is not UAT PASS, merge approval, first-cohort release approval, production/runtime/cron authorization, or final product acceptance.

## Entry

- Local replay page: `generated/multimodal/D36/replay.html`
- Route: 贝尔格莱德 → 布达佩斯 → 维也纳
- Build status: `complete`
- Review scope: local/private review unless explicitly approved otherwise

## Tested Viewports

- Primary mobile viewport: 390x844
- Additional manual viewports may be added by Jarvis/OpenClaw during final UAT.

## Feature Checklist

- Replay page opens locally
- Cue count: 9
- Memory cards available: 16
- Media metadata items available: 9
- Route segments available: 6
- Narration variants available: 4
- P1b panels available: Cards, Route, Media, Variants
- Audio.currentTime cue sync remains the playback driver
- Browser smoke evidence should include screenshot, DOM summary, and console summary when tooling is available
- Default replay hides Cards/Route/Media/Variants debug panels; append `?debug_info=true` to show them for testing.

## Known Limitations

- Audio is present for this local build.
- Generated media and local images are ignored outputs and are not committed.
- This package does not implement feedback intake, database storage, issue automation, weekly review, AR, VR, or wearable flows.
- Browser smoke evidence is generated outside the builder to keep normal local builds independent of browser tooling.

## Privacy

- Shareability status: local/private review.
- Do not publish screenshots, generated media, audio, local images, or generated directories without explicit approval.
- Do not paste credentials, local absolute paths, or private itinerary details into user feedback.

## Acceptance Decision Options

- ACCEPT_FOR_FIRST_COHORT
- NEEDS_FIX
- BLOCKED
