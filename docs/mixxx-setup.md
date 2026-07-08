# Splode Lab Live + Mixxx setup

Use this to connect Mixxx to Splode Lab Live for audio-reactive visuals and MIDI timing.

Mixxx provides the music playback. Wave Link handles audio routing. MIDI timing uses loopMIDI on Windows, or the IAC Driver on macOS.

[Mixxx](https://mixxx.org/download/) is free, open-source DJ software for Windows, macOS and Linux. [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html) creates virtual MIDI ports on Windows so apps can send MIDI to each other. macOS already includes the [IAC Driver](https://support.apple.com/guide/audio-midi-setup/transfer-midi-information-between-apps-ams1013/mac) for MIDI between apps: one app sends MIDI to an IAC bus while another app receives from that bus.

## Windows

### Install

- [Mixxx](https://mixxx.org/download/)
- [Wave Link](https://www.elgato.com/us/en/s/downloads)
- [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html)
- Splode Lab Live

### Audio connection

1. Open Wave Link.
2. Create a mix called Splode-Mix.
3. Add Mixxx to that mix.
4. Set Wave Link monitoring to your speakers or headphones.
5. In Splode Lab Live, choose the Wave Link / Splode-Mix device as the audio input.
6. Play a track in Mixxx.
7. Check that Splode Lab Live shows audio activity.

### MIDI connection

1. Open loopMIDI.
2. Create a port called SplodeLab Sync.
3. Leave loopMIDI running.
4. Open Mixxx.
5. Go to Preferences > Controllers.
6. Select SplodeLab Sync.
7. Load the Mixxx MIDI mapping/script for light mapping.
8. Apply the controller setup.
9. In Splode Lab Live, choose SplodeLab Sync as the MIDI input.
10. Play a track in Mixxx.
11. Check the Splode Lab Live MIDI log.

## macOS

### Install

- [Mixxx](https://mixxx.org/download/)
- [Wave Link](https://www.elgato.com/us/en/s/downloads)
- Splode Lab Live

### Audio connection

1. Open Wave Link.
2. Create a mix called Splode-Mix.
3. Add System Audio to that mix.
4. Set Wave Link monitoring to your speakers or headphones.
5. Open System Settings > Sound > Input.
6. Choose the Wave Link / Splode-Mix input.
7. Open System Settings > Sound > Output.
8. Choose your normal speakers or headphones.
9. In Splode Lab Live, choose the same Wave Link / Splode-Mix device as the audio input.
10. Play a track in Mixxx.
11. Check that Splode Lab Live shows audio activity.

### MIDI connection

1. Open Audio MIDI Setup.
2. Choose Window > Show MIDI Studio.
3. Double-click IAC Driver.
4. Turn on Device is online.
5. Add or rename a bus called SplodeLab Sync.
6. Open Mixxx.
7. Go to Preferences > Controllers.
8. Select IAC Driver / SplodeLab Sync.
9. Load the Mixxx MIDI mapping/script for light mapping.
10. Apply the controller setup.
11. In Splode Lab Live, choose IAC Driver / SplodeLab Sync as the MIDI input.
12. Play a track in Mixxx.
13. Check the Splode Lab Live MIDI log.

## Launchpad Mk3 Mini lighting feedback

Splode Lab Live has built-in lighting feedback for the Novation Launchpad Mini Mk3. It relays MIDI to OSC using [Conduit](https://github.com/sndwrks/conduit) with the mappings in this repo, including the [Launchpad Mk3 Mini mapping](../conduit/LaunchPad%20Mk3%20Mini/mapping/mapping.json). Conduit is a great way to drive Splode Lab Live's OSC interface.

Conduit must be running for the pad lights to react. If it is not running, the app still works, but the Launchpad pads will not light up.

1. Install and open [Conduit](https://github.com/sndwrks/conduit).
2. Connect your Launchpad Mini Mk3.
3. Load the Launchpad Mk3 Mini mapping.
4. Leave Conduit running.
5. Open Splode Lab Live.
6. Check that the Launchpad pads light up in response to activity.

## Check

Audio is working when Splode Lab Live shows incoming audio levels.

MIDI is working when Splode Lab Live logs incoming MIDI messages from the sync port.

Audio and MIDI are separate:

- Audio drives audio-reactive visuals.
- MIDI carries timing/control data such as BPM, beat, MIDI Clock or MTC.
