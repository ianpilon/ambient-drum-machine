# Ambient Drum Machine

A one-voice drum machine for slow, sparse, half-time ambient: a two-tone sub kick on a 16th grid, a bed of crackle where the hi-hats would be, and an optional swell. Built from a signal analysis of SVLBRD's "Hvit" (HBTL, 2016) rather than from samples.

**Play it:** https://ianpilon.github.io/ambient-drum-machine/

Open `index.html` in a browser. No build, no server, no dependencies. Press space or flip Run.

## What the analysis found, and what the machine does with it

- **Grid.** 65 BPM, strict 16th grid, 4-bar loop. Hits in the source were quantized within 3 ms. The Calm and Busy patterns are lifted straight from the track.
- **One drum.** A short two-tone kick: about 52 Hz gliding down, plus a partner near 86 Hz (a major sixth up) that decays faster. About 170 ms to silence, no click, sits only a few dB above the pad. Knobs: Tune, Partner, Decay, Knock (30 ms mid-range body), Room (short dark reverb send), Level.
- **Dust.** Non-rhythmic sub-millisecond clicks above 3 kHz, doing the job hi-hats would do without ever giving you a pulse to count. Knobs: Density, Bright, Level.
- **Swell.** The "slow crash" in the source is not a cymbal. It is the drone's upper partials (D5 to A5) rising over 0.4 s and falling over 1.6 s about six times a minute, unlocked from the kick. Off by default. Knobs: Every, Dark, Level.
- **Mutate.** Every pass drops one hit and adds one on an "e" or "a" position, so the loop never repeats exactly.
- **Loose** adds up to 20 ms of timing slop. **Tempo** runs 50 to 90. A limiter on the master lets the loud hits kiss 0 dBFS.

Tap a step to cycle rest, soft, mid, loud.

The panel reuses the visual language and controls of [Shruti 4](https://github.com/ianpilon/shruti-4).
