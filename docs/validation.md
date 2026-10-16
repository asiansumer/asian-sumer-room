# Validation snapshot

[Back to the project](../README.md)

**Recorded: 15 October 2026.** This is a dated summary from the private implementation workspace, not a public CI badge or an independently reproducible test suite.

| Check | Recorded result | Scope |
| --- | ---: | --- |
| Project tests | 104 passed | Navigation, asset contracts, audio state, game records, archive/content behavior and mobile resource budgets. |
| Original hosting adapter tests | 8 passed | Retained fallback adapter behavior; the live site now uses independent Cloudflare hosting. |
| Cloudflare adapter tests | 4 passed | Owner-token validation, protected routes, content writes and Portfolio routing. |
| Production build | Passed | Vite build and deployment packaging; a bundle-size advisory remains. |

## Browser evidence

- The live site was captured on 15 October 2026 at the browser's default 1280 × 720 viewport. Gallery images are direct captures, not generated redesigns.
- The current game starts inside Studio Display. Manual expansion and collapse were checked; the nickname prompt remains present. The deployed application bundle matched the local build during verification.
- The mobile repair was checked at 402 × 874 and 874 × 402. Initial overview had zero WebGL canvases; selecting a scene loaded the mobile room. Desk, Records, Contact and Archive navigation completed without console errors in that session.
- Production health and the mobile GLB hashes were checked after deployment. These checks establish serving/data-integrity behavior, not global uptime.

## Limits

- Desktop browser viewport testing does not reproduce an iPhone's GPU, WebKit process limits or thermal behavior. Physical iPhone confirmation remains pending.
- The texture numbers are calculated image-storage budgets, not actual Safari memory samples or FPS benchmarks.
- Audio tests cover coordination and failure behavior; the silent tour does not verify sound quality or every device's playback policy.
- The leaderboard accepts a browser-reported score with basic server checks. It is not cheat-proof.
- No accessibility certification, award, traffic, conversion or universal device-compatibility claim is made here.

## Media in this repository

`overview.jpg`, `records.jpg`, `desktop.jpg`, `arcade.jpg` and `films.jpg` are screenshots of the running site. `room-tour.mp4` is a 30-second silent edit of actual browser captures, including camera movement, sleeve selection and film browsing. Opening and closing overview shots are held briefly. The capture frame rate varies; the video is not a performance benchmark.
