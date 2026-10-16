# Asian Sumer — The Room

A personal website built around my apartment, connecting music, independent projects and the things I keep returning to.

**[Explore the room ↗](https://asiansumer.com/)** · [30-second tour](assets/room-tour.mp4) · [Engineering notes](docs/engineering.md) · [中文](README.zh-CN.md)

![The live website: an apartment overview with entrances to the desk, music, films, records and contact.](assets/overview.jpg)

## Why a room?

My previous website read like a résumé. I wanted a place that could hold more of me: the music I make and play, the projects I work on, and the books and films that stay with me.

The apartment gives those things a physical home. A record drawer becomes a music collection. A computer becomes a place to explore projects or play a game. Visitors choose a corner and move between deliberately framed views.

## Inside

| Corner | What happens there |
| --- | --- |
| **Records** | Browse stacked sleeves, choose a record and set the soundtrack for the rest of the visit. |
| **Music** | Listen to my recorded DJ sets, with waveform seeking and playback that continues across the room. |
| **Desk** | Open an interactive Studio Display, explore projects or play Dino Runner with a shared leaderboard. |
| **Films** | Scroll through a film shelf on the television; each film links to its Douban page. |
| **Contact** | Open the phone on the bedside table to find my profiles and portfolio. |
| **Archive** | Discover a quieter space for books, unfinished demos and work in progress. |

![A selected sleeve from my own album, above the open record drawer.](assets/records.jpg)

![The interactive desktop fitted to the physical monitor in the room.](assets/desktop.jpg)

The [silent tour](assets/room-tour.mp4) uses captures from the running website. The overview is a rendered image of the apartment model; the interior scenes and transitions are real-time 3D.

## Three engineering decisions

**Make the screen a usable interface.** The monitor's four corners are projected into browser coordinates, and a single CSS projective transform aligns the HTML surface with the 3D screen. Forms, links and the game stay interactive inside the room.

**Treat music as part of the visit.** Playback lives beyond individual scene panels. An explicit change of source prepares the new audio, fades and pauses the old source, then starts the new one. Request versions prevent a slow, older action from taking over later.

**Budget for decoded assets.** A reported mobile Safari crash prompted a separate mobile asset path. For the main room, the estimated RGBA-plus-mipmap texture budget dropped from **1,116 MiB to 134 MiB**, about **88%**, while preserving geometry and desktop assets. This is an asset-size calculation, not a measured Safari memory benchmark; physical-device confirmation remains pending.

[Read the decisions and trade-offs →](docs/engineering.md)

## Built with

**React · Three.js · Blender · Vite · Cloudflare Workers · D1 · R2**

Blender supplies the room assets and baked lighting. React and Three.js connect the authored views, object interactions and HTML screens. Cloudflare hosts the application, shared game records, editable content and media.

## My role & process

I defined the apartment concept, supplied room references and personal content, directed the visual and interaction choices, and reviewed the experience through repeated iteration. Development was AI-assisted: Codex helped with implementation, scripted Blender modeling, debugging, tests and deployment. This showcase distinguishes the product decisions I directed from the implementation tools and third-party components used.

## Status & scope

The website is live and continues to evolve. The latest recorded validation on **15 October 2026** includes **116 passing automated checks** across the project and deployment adapters, plus browser checks. [Validation details and limits](docs/validation.md) are documented separately.

**This repository contains project documentation and demos. The application source code and original assets are private.** It is a showcase, not a runnable source release. See [credits and media notes](docs/credits.md).

---

[Website](https://asiansumer.com/) · [Portfolio](https://asiansumer.com/portfolio/) · [GitHub](https://github.com/asiansumer)
