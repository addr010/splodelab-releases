# Splode Lab Live

Free desktop VJ software, made by one retired coder for the live visuals community.

Since 2010 I've been building and giving away free VJ tools. Splode Lab Live is my main desktop app: clip decks, MilkDrop presets, ISF shaders, JavaScript motion graphics and audio reactivity, all in a lightweight package that just works. No subscriptions, no accounts.

A sibling to **[Splode Lab EX](https://apps.apple.com/app/splode-lab-ex/id1275951874)**, the real-time visual effects app for iPad & iPhone (4.6 stars on the App Store). Same name, different app.

[Download Splode Lab Live](https://splodelab.com/) &nbsp;·&nbsp; [Splode Lab EX for iPad](https://apps.apple.com/app/splode-lab-ex/id1275951874)

## What is Splode Lab Live?

A desktop app for VJs, musicians, hobbyists and live performers who want responsive visuals without a huge workflow. Open the app, choose your audio input (or just play music on your computer), and the visuals start reacting straight away. Drop in video clips, MilkDrop presets or ISF shaders and you're performing in seconds.

I built it to be used on stage, not just for pretty renders.

### What it does

- Clip decks for video and VJ loops, with easy switching and layering
- Strong MilkDrop 2 preset support
- Full ISF shader support
- JavaScript for your own custom motion graphics
- Real-time audio reactivity from input or file playback
- OSC and MIDI control
- Auto-play mode so you can focus on the music
- Open and hackable on purpose

### Vodl scripting

Write a `.vudl.txt` file to choreograph every layer at once. Expressions, envelopes, oscillators and shader params. Save the file and it hot-reloads live.

```text
# Star clip on L1 loops and spins; L2 title fades.

.env(titleIn,
  0% 0
  100% 1 easeInOut
)

L1:
  <[a b c]*4>
  rotation saw.every(3 bar)*180
  scale 1 + tri.every(1 beat)*0.12

L2:
  positionY 0.35
  opacity env(titleIn 2:1->3:1)
```

## Download

Get the latest release for Windows or macOS from the [download page](https://splodelab.com/).

### Installation

**Windows:**
1. Download the .exe
2. Run it. Windows may show a SmartScreen warning. Click "More info" then "Run anyway"

**macOS:**
1. Download the .zip
2. Unzip and move it to Applications
3. Right-click and select "Open" on first launch to get past Gatekeeper

## System requirements

- **Windows:** Windows 10/11 (64-bit)
- **macOS:** macOS 11 (Big Sur) or later (Apple Silicon)
- **GPU:** OpenGL 3.3+ compatible graphics card

## Local music analysis (optional)

The music sync button analyzes a song into beats and bars so the transport locks to the actual track. To enable it, install Python:

1. Install Python 3.10+ and make sure `python3` is on your PATH
2. `pip3 install librosa`

That's it. If analysis fails, the app log records why.

## Community & support

- Found a bug? [Open an issue](https://github.com/addr010/splodelab-releases/issues).
- If the app is useful and you want to support development, there's a [Buy Me A Coffee](https://buymeacoffee.com/gammaridersworld). A simple thanks is just as good.

## The Splode Lab family

- **Splode Lab Live**: free desktop app for Windows & macOS (this repo).
- **[Splode Lab EX](https://apps.apple.com/app/splode-lab-ex/id1275951874)**: real-time visual effects for iPad & iPhone on the App Store. 4.6 stars. Draw with fire, tap explosions, and export video loops for your VJ software.

Two different apps under one name. Pick whichever fits what you're doing.

## About

This repository hosts the release builds and download page for Splode Lab Live, a free project from Six Foot Games. Made with love by one stubborn coder.
</content>
