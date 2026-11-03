---
layout: post
title:  "Bevy Periscope"
date:   2026-11-03 09:00:00 +0000
categories: projects bevy
---
A web tool for looking inside a [Bevy](https://bevy.org) game while it runs. It connects over the Bevy Remote Protocol, so the game needs no extra plugin.

<video src="{{ '/assets/bevy-periscope/periscope-demo.mp4' | relative_url }}" poster="{{ '/assets/bevy-periscope/periscope-demo-poster.jpg' | relative_url }}" controls autoplay muted loop playsinline width="1280" height="720" style="max-width: 100%; height: auto;">
  <img src="{{ '/assets/bevy-periscope/periscope-demo.gif' | relative_url }}" alt="Bevy Periscope connecting to a Bevy app, then plotting entities live, editing a component, running a query, showing system data flow and spinning a globe">
</video>

*An 83-second tour, recorded against a test world of about 240 entities.*

## What the video shows

1. **Connect.** Point Periscope at a running app's BRP port.
2. **Watch it live.** Entities are plotted by position, and move as the game runs.
3. **Change it.** Editing a boss's `Transform` moves the boss and its squad across the map.
4. **Ask questions.** A query finds every entity with `Health.current` below 10.
5. **See how it fits.** The data flow view shows which systems write the `GameClock` resource.
6. **Go global.** Geographic data is plotted on a 3D globe.

## Features

- **Map:** see your world as a hierarchy, by archetype, as a spatial map, as system data flow, or on a 3D globe.
- **Entities and resources:** browse and search them, and inspect their values. The inspector follows the selected entity live.
- **Query:** build `with`, `without` and value filters, with paged results that can refresh live.
- **Edit:** change fields, lists, maps and enums, add and remove components and resources, and spawn and despawn entities.

Periscope runs locally as a static web app, and your app doesn't depend on it. It targets Bevy 0.20.
