<p align="center">
  <img src="icon.png" width="128" height="128" alt="Ambient Witness icon">
</p>

<h1 align="center">Ambient Witness</h1>

<p align="center">
  A macOS screen capture daemon that builds a searchable visual timeline of everything you do on your computer.
</p>

<p align="center">
  <a href="https://github.com/thieso2/AmbientWitness/releases/latest">Download</a>
</p>

---

## What is Ambient Witness?

Ambient Witness runs quietly in the background on your Mac, continuously recording display frames, running OCR on what's on screen, and collecting system metadata — giving you a complete, searchable record of your computing history.

Think of it as a flight recorder for your desktop.

## Features

- **Continuous screen capture** — snapshots display frames as JPEG images, assembled into HLS (fMP4) segments for efficient storage and playback
- **OCR pipeline** — extracts text from keyframes using Apple's Vision framework, so you can search for anything you've seen on screen
- **System metadata collection** — records active windows, apps, browser tabs, power state, audio playback, Wi-Fi, location, and user activity
- **Browser extension** — deep integration with Chromium browsers (Chrome, Brave, Edge, Dia, Arc, Vivaldi) captures tab navigation, focus spans, and page interactions
- **MCP server** — exposes captured data via Model Context Protocol so AI assistants can query your timeline
- **Privacy-first** — all data stays on your machine in `~/Library/Application Support/Engram/data/`
- **Power-aware** — media assembly runs only on AC power to preserve battery life

## Requirements

- macOS 15.0 (Sequoia) or later
- `ffmpeg` on PATH (for media assembly)

## Install

1. Download the latest `.zip` from [Releases](https://github.com/thieso2/AmbientWitness/releases/latest)
2. Unzip and move `Ambient Witness.app` to `/Applications`
3. Launch and grant the requested permissions (Screen Recording, Accessibility, Location)

## Permissions

Ambient Witness needs three system permissions to function:

| Permission | Why |
|---|---|
| **Screen Recording** | Capture display frames for the visual timeline |
| **Accessibility** | Read window titles, browser tabs, and app state |
| **Location** | Record where you work and read Wi-Fi network names |

## Data & Privacy

All captured data is stored locally in date-partitioned directories under `~/Library/Application Support/Engram/data/`. Nothing is uploaded anywhere. The browser extension includes configurable domain blocklists, query string redaction, and incognito exclusion.

## License

Proprietary. All rights reserved.
