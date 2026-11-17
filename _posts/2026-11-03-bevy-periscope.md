---
layout: post
title:  "Bevy Periscope"
date:   2026-11-03 09:00:00 +0000
categories: projects bevy
---
I've been spending a lot of time on Bevy ECS projects lately. As they've grown, they've become harder to reason about. I wanted a better way to see how systems interact, how entities move, and what's in my components and resources.

I tried the existing tools, but none of them fit my workflow:

- **[bevy-inspector-egui](https://github.com/jakobhellermann/bevy-inspector-egui):** it draws its UI inside the app's window, and my apps are mostly headless.
- **[vscode-bevy-inspector](https://github.com/splo/vscode-bevy-inspector):** I don't use VS Code, and didn't want to open it just for this.
- **[bevy_inspector.nvim](https://github.com/Lommix/bevy_inspector.nvim):** Neovim is my daily driver, and I've been using this one, but it can't query components, and it has no hierarchy, archetype, spatial, data flow or globe views. I also felt constrained to working inside Neovim.

So I built [Bevy Periscope](https://github.com/Jammors/bevy-periscope), a web-based tool for visualising Bevy ECS apps. It talks to your app over the Bevy Remote Protocol (BRP), so the only change your app needs is enabling Bevy's remote plugins.

<video src="{{ '/assets/bevy-periscope/periscope-demo.mp4' | relative_url }}" poster="{{ '/assets/bevy-periscope/periscope-demo-poster.jpg' | relative_url }}" controls autoplay muted loop playsinline width="1280" height="720" style="max-width: 100%; height: auto;">
  <img src="{{ '/assets/bevy-periscope/periscope-demo.gif' | relative_url }}" alt="Bevy Periscope connecting to a Bevy app, inspecting a unit live, moving it on the map, running a query, browsing the hierarchy and archetypes, showing which systems use a resource, watching and sending events, and zooming into a detailed globe">
</video>

*A tour, recorded against a test world of about 240 entities.*

Periscope runs locally as a static web app, and your app doesn't depend on it. At the time of writing, it targets Bevy 0.20. For the current feature list and setup instructions, see the [README](https://github.com/Jammors/bevy-periscope).
