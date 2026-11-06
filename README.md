<div align="center">
  <img src="branding/golfcaddie-logo.png" alt="GolfCaddie logo" width="140">
  <h1>GolfCaddie</h1>

  <p><strong>Your personal golf assistant.</strong></p>

  <img src="https://img.shields.io/badge/status-Beta%20%28TestFlight%29-029447?style=flat-square" alt="status"> <img src="https://img.shields.io/badge/platform-iOS%2017%2B-035229?style=flat-square" alt="platform"> <img src="https://img.shields.io/badge/license-proprietary-555555?style=flat-square" alt="license"> <img src="https://img.shields.io/badge/by-Aquila%20Digital%20LLC-14213D?style=flat-square" alt="Aquila Digital LLC">
</div>

> **Showcase repository.** The source code for GolfCaddie is not published. This page presents what the product is and how it works.

## Screenshots

<p align="center">
  <img src="docs/screenshots/1-know-the-number.png" width="30%" alt="Round screen: real yardage, plays-like number and club pick">
  <img src="docs/screenshots/2-ask-your-caddie.png" width="30%" alt="Conversational caddie">
  <img src="docs/screenshots/3-your-bag.png" width="30%" alt="Your bag with learned distances">
</p>

<p align="center"><a href="docs/media/golfcaddie-motion-ad-dark.mp4"><b>▶ Watch the 20-second motion ad</b></a> (dark mode)</p>

## Overview

An AI caddie for iPhone that knows your game, reads wind and elevation, and talks you through every shot by voice or text. Club selection is deterministic math; the language model only handles the human side.

## How it works

```mermaid
flowchart LR
  A["GPS + OSM course data + weather + your learned carries"] --> B["CaddieEngine computes plays-like distance and club pick (deterministic, unit-tested)"] --> C["CaddieReasoner grounds the answer (club call, rules, strategy)"] --> D["Apple Intelligence phrases it naturally, fully on-device"]
```

## Features

- Rangefinder with plays-like distance (wind, temperature, altitude, elevation, lie)
- Round screen: satellite hole view, front/middle/back, tap-to-target, hazard carries, shot tracking, scoring
- Conversational caddie with hold-to-talk voice and optional spoken replies
- Plain-language rulebook covering all 25 Rules of Golf plus a strategy playbook
- Bag management that learns your real carry distances
- Tournament Mode, handicap and scoring stats, Apple Watch companion target
- Auto-loaded hole maps from OpenStreetMap; offline-capable

## Tech stack

| Layer | Choice |
|---|---|
| Language / UI | Swift, SwiftUI, iOS 17+, Xcode 26 |
| AI | Apple Intelligence (on-device) + deterministic engine |
| Data | MapKit, OpenStreetMap, WeatherKit, Open-Meteo elevation |
| Platforms | iPhone + Apple Watch target |
| Backend | None in v1 (CloudKit foundation paused) |

## Privacy & security

Nothing leaves the phone for the caddie. No account in v1.

## Brand

| | Name | Hex | Role |
|---|---|---|---|
| <img src="https://placehold.co/44x22/035229/035229.png" alt="#035229" /> | Forest | `#035229` | Primary / text |
| <img src="https://placehold.co/44x22/029447/029447.png" alt="#029447" /> | Fairway | `#029447` | Accent |
| <img src="https://placehold.co/44x22/38B34A/38B34A.png" alt="#38B34A" /> | Grass | `#38B34A` | Highlights |
| <img src="https://placehold.co/44x22/C8E2D2/C8E2D2.png" alt="#C8E2D2" /> | Mint | `#C8E2D2` | Light surfaces |

**Mark.** Condensed heavy GOLFCADDIE wordmark; display type echoes it, numbers in SF Rounded with monospaced digits.

**Voice.** Direct, calm and confident, like a good caddie: the number, the club, the reason.

## Roadmap

- Friends & social feed (needs backend + moderation)
- Apple Watch yardages with wrist tap
- Green reading and pin position
- Strokes Gained analytics
- Android
- Downloadable on-device model for non-Apple-Intelligence iPhones

## Notes

Marketing assets (launch kit, ads, videos, landing page) are kept in a separate private folder, not in this repo.

## License

Proprietary. Shared publicly for portfolio and demonstration purposes only. See [LICENSE](LICENSE).

---

<div align="center">

Built by [Aquila Digital LLC](https://github.com/Steven6Brown) · *Per Aspera Ad Astra*

</div>
