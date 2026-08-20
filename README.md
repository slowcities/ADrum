# ADrum

Four percussion voices with AD envelopes. A drum synthesizer that runs in a browser, built as a teaching instrument.

One HTML file. No install, no build step, no account, no cost. Open the link and it makes sound.

**▶ Play it here** (https://slowcities.github.io/ADrum/)

---

## Why this exists

A class learning electronic music needs more than one kind of player. [4LS](https://slowcities.github.io/4LS/) teaches pitch and timbre; this teaches rhythm and time; [16Max](https://slowcities.github.io/16max/) keeps the clock. Together they let a group of students perform as an ensemble rather than taking turns at one instrument.

The name is the design. Every voice is an **A**ttack and a **D**ecay and nothing else — no sustain, because a struck drum does not hold. It sounds, and it dies away. Once that is on the panel, the rest of the instrument follows from it.

Like 4LS, this is deliberately one instrument rather than a suite of tools. Everything on the panel is there because it teaches something.

The central idea is that a drum kit is not a collection of different machines. A kick and a tom are the same engine with different Decay times. A snare and a floor tom are the same engine with different Cutoff settings. Any voice can run any engine, so students discover this by doing it rather than being told.

---

## What it is

Complete and working. Four voices, each with:

- A switchable engine — Pitched decay, Noise, or Metal
- An AD envelope with a Snappy/Slow range switch
- One filter, low pass or high pass
- Its own delay
- Level and Pan

Played by pads, computer keyboard, or MIDI, with MIDI learn across every slider and every pad, soft takeover on the sliders, and the help system in six languages.

Controls are sliders rather than the rotary knobs used in 4LS. This is a decision rather than a gap: a voice panel here has a dozen parameters and four of them stack on a phone screen, and sliders read at a glance in a column where knobs do not.

The five non-English translations have not been reviewed by a native speaker.

---

## Languages

The help text is available in English, Español, 한국어, العربية, 中文, and 日本語. The language buttons appear on the start screen and again in the help bar once Help is on; the choice is remembered on that computer.

Translated: every help panel, the start screen, and the engine description that changes as you switch a voice between architectures. Arabic help reads right to left.

Control labels stay in English on purpose — Attack, Decay, Cutoff, Resonance, Pan, Level. That vocabulary is shared across instruments and mixing desks worldwide, so a student who learns it here can walk up to any hardware drum machine or mixer in any country and read the panel. The help text explains those words in the reader's own language rather than replacing them.

---

## Getting started

1. Open the link. Click **Start the engine** — browsers require a click before audio can begin.
2. Hit the pads, press the **A S D F** keys, or plug in a MIDI controller.
3. Turn on **Help** to read what each section does.
4. Change one thing on one voice and listen to what happened.

Headphones recommended. Start with the volume moderate — resonance and delay feedback both add level.

---

## Playing it

| Input | How |
| --- | --- |
| Pads | Click or tap. Multi-touch works, so several pads at once are fine on a phone or tablet |
| Computer keyboard | **A S D F** — one key per voice |
| MIDI notes | Notes 36, 38, 42, 45 map to voices 1–4. Any other note falls through to a voice in the order it first arrives, so a controller of any layout still plays |
| MIDI learn | Assign hardware knobs to any slider, and hardware pads to the four voice pads — see below |
| Silence | Stops everything and clears the delay lines |

**MIDI learn:** click MIDI learn in the top right, click any slider or pad on screen, then move the knob or hit the pad you want on your controller. The assignment appears as a small badge — CC for a knob, N for a note. Clicking an assigned control a second time removes it; Clear all wipes every assignment; Escape backs out. Assignments are saved in the browser, so a rig set up once comes back the next time you open the page on that machine. The Master control can be assigned too.

The four pads are assignable as well, and they are **momentary**: they fire on the press and ignore the release. A drum voice is a one-shot with no sustain, so there is nothing for a release to end and nothing a toggle could usefully latch.

Sliders take a knob and pads take a note, and neither will accept the other. A note carries no position for a slider to follow, and a knob has no press for a pad to answer, so pairing them the wrong way round would produce a mapping that could never behave sensibly.

Anything left unassigned still follows the General MIDI layout, so a controller works the moment it is plugged in and learning stays optional. A learned assignment always takes priority over that default.

Assigned controls use **soft takeover**: after a reload or a drag on screen, the hardware knob is no longer where the slider is, so it does nothing until you sweep it onto the current value and pick it up. While it is waiting, a small marker on the slider track shows where the hardware is sitting, so you know which way to turn. This means a controller sitting in the wrong position never yanks a voice out of shape the moment it moves.

There are around fifty assignable controls and most hardware has sixteen knobs, so mapping everything is not the goal. Pick the handful a performance actually needs — usually Decay, Cutoff, and Level across the four voices — and leave the rest to the screen.

There is no sequencer, and this is a decision rather than an omission. Every hit happens at the moment a student makes it, so the timing belongs to the player. It also means the instrument behaves identically alone and in a group — nothing has to be synchronized, because nothing is running on its own.

Sequencing lives in [16Max](https://slowcities.github.io/16max/) instead, where it is the whole subject rather than a feature bolted onto something else. In a group, the usual arrangement is that one device runs 16Max into the PA and everyone else plays ADrum and 4LS by hand over it.

---

## The panel

Four identical voice panels. Each one is a complete little drum machine: an engine, an envelope, a filter, a delay, and a place in the mix.

### Oscillator

Where the sound is born. Three engines, and any voice can run any of them:

**Pitched decay** — one sine, pulled down by a fast pitch envelope. A long Decay gives a kick, a short one gives a tom, an extreme Bend gives a zap. Tune sets the pitch it lands on, Bend how far above it starts, Bend fall how quickly it arrives.

Tune reads in hertz with the note it lands on beside it — `55 Hz (A1)`. Most settings fall between two notes rather than on one, and the gap is shown in cents rather than rounded away, because a student reading `A♯1` at 58 Hz would otherwise conclude that 58 Hz simply is A♯1. A hundred cents is a semitone. The four voices ship tuned to notes, with the kick at A1 and the tom at D3, an octave and a fifth apart.

**Noise** — no pitch at all. Colour tilts it from a dark rumble to full white before the filter shapes it. The level is compensated as Colour moves, so turning it down gets darker rather than merely quieter.

**Metal** — six square waves at ratios that never line up, so no fundamental ever forms. High pass it short for a hat, or let it ring for a bell.

Controls that an engine does not read are greyed rather than left sitting there doing nothing.

### Envelope

**Attack** is how fast the sound arrives, **Decay** how fast it falls away. There is no sustain and no release, because there is nothing to hold.

**Snappy / Slow** moves both times into a shorter or a longer range. The number shown is what the engine actually receives, so switching modes changes the reading as well as the sound — the label never claims something the DSP is not doing.

### Filter

One filter per voice, switchable between low pass and high pass. Low pass keeps what lies below the cutoff and darkens the sound; high pass keeps what lies above and thins it. Resonance lifts the frequencies right at the cutoff, and high enough it makes the filter ring on its own.

### Delay

An echo, one per voice. Time sets the gap between repeats, Feedback how many there are, Mix how loud they come back. At Mix zero there is no delay at all, which is where every voice starts.

There is no send control, because a dedicated delay line does not need one — Send and Mix would multiply into a single wet level and give the same result twice over.

### Output

**Level** and **Pan** — a mixer in two controls. Level is how loud a voice sits against the other three; Pan places it left or right. Balancing a kit is nothing more than these two, used carefully.

Pan is equal-power, so a voice swept across the field holds a steady loudness instead of dipping in the middle.

---

## Presets

Six kits, each demonstrating one idea, all built from the same panel.

**Standard kit** — a kick, a snare, a hat and a tom, each on a different engine. The panel as it opens.

**Tuned kit** — all four voices pitched, on an A minor triad spanning two octaves, with the bend pulled right back and the decays long enough to actually hear a pitch. Panned apart so the chord occupies a space rather than a point.

**All noise** — the one to load first. Four voices on the same engine, differing only in Colour, filter and Decay, and yet a kick, a snare, a hat and a wash come out of it. This is the clearest demonstration the instrument has.

**Boom** — slow mode, low tunings, decays running to three and a half seconds. Percussion long enough to become drone.

**Bells** — all four on the metallic cluster, high passed and left to ring for a second or more. The same engine that makes a hat when it is cut short.

**Dub delay** — the kick stays dry so the pulse holds, and everything else is thrown into its own delay at a different rate. That difference is what makes four voices sound like a room rather than a line.

Kits are not saved between sessions. This is deliberate: it keeps the file self-contained and keeps students building rather than recalling.

---

## Teaching with it

Some sequences that work:

**A kick and a tom are the same thing.** Set two voices to Pitched decay with identical settings. Change nothing but Decay on one of them. The distinction students think of as two instruments is one number.

**A snare and a floor tom are also the same thing.** Take the Noise voice, switch the filter to Low pass, drop the Cutoff, lengthen the Decay. The snare becomes a floor tom without changing engines.

**Why a hi-hat has no pitch.** Play the Metal engine, then try to sing along with it. Students cannot, and the reason is on the panel: six oscillators at ratios that never line up, so the ear has no fundamental to lock onto.

**Drums have pitch too.** Set two voices to Pitched decay and tune them by the note readout rather than by ear — a kick at A1 and a tom at E2 is a fifth. Then detune one by fifty cents and listen to the pair sour. Percussion is not exempt from tuning, and the cents readout is where that becomes obvious.

**One engine, four drums.** Load All noise and look at the four panels. Every voice is on the same engine. The only differences are Colour, the filter and the Decay, and those three controls are the whole distance between a kick and a hi-hat.

**When does a drum stop being a drum?** Load Boom and lengthen the decays further. At some point the class stops calling it percussion and starts calling it a drone, and there is no line in the code where that happens — only a number getting larger.

**What an envelope is.** Attack all the way down and Decay short is a click. Attack up is a swell. Same engine, same filter — the envelope alone is the difference between a drum and a pad.

**What a mixer does.** Give four students one voice each and have them balance the kit by ear using only Level and Pan. Then have them do it again with headphones swapped for a single speaker, and discuss why the Pan work disappeared.

**What feedback is.** Short Time, high Feedback, one hit. The room fills up from a single strike. Then ask why it stops growing.

---

## Requirements

Any current browser: Chrome, Edge, Firefox, or Safari 14.1+. Works on phones and tablets, and multi-touch is handled per finger, so chords of drums work on a touch screen.

MIDI input requires a browser with WebMIDI (Chrome and Edge; Firefox and Safari do not currently support it). This covers both note triggering and MIDI learn. Everything else works everywhere.

Pan requires headphones or two speakers. Through a single phone speaker it will sound like nothing is happening.

---

## Hosting it yourself

The whole instrument is one file. Fork this repo, enable GitHub Pages in Settings → Pages, and it is live.

**Do not open the file directly from your hard drive.** A `file://` page has no real origin, and browsers refuse to load the AudioWorklet that generates the audio. The panel will appear and nothing will make sound. Serve it over HTTP instead — GitHub Pages, or locally:

```
python3 -m http.server 8000
# then open http://localhost:8000
```

The engine tries a `data:` URL as a fallback when the usual `blob:` route is blocked, which rescues some cases, but a real origin is the reliable answer.

---

## Under the hood

The entire drum engine is a single AudioWorklet processing all four voices inline, rather than a graph of Web Audio nodes. Same reasoning as 4LS: CPU headroom on school hardware, and precise control over the DSP.

- **Square waves are PolyBLEP band-limited**, so the Metal engine stays clean instead of aliasing into a mess at high tunings.
- **Filters are TPT state-variable**, one per voice, with a saturator in the resonant path so high resonance settles at a stable amplitude rather than running away.
- **Envelope times are calibrated to the labels.** A Decay reading 0.5 s falls to 1% of its starting level in 0.5 s. This is the same correction 4LS uses, carried across deliberately — the first implementation there ran roughly four and a half times slower than its label claimed, and inheriting the corrected constant means the bug cannot reappear here.
- **Delay feedback is capped and the write is limited**, so a delay tuned to reinforce itself gets loud and then sits, rather than climbing without limit. A limiter also sits on the master, linear below its knee so ordinary playing passes through untouched.
- **Noise level is compensated from the one-pole's own RMS**, so Colour changes the character rather than the volume.
- **Pan is equal-power** — a sine and cosine pair rather than linear gains, which would dip audibly at centre.

---

## Design principles

- **Zero friction.** One file, no build, no install, no accounts. If a student can open a link, they can use it.
- **Visible consequence.** Every control shows its effect somewhere on screen, and every label reports what the engine actually received.
- **Restraint.** One instrument built well. No sequencer, no sampler, no second filter. Features are not added because they would be impressive.
- **Free access.** The barrier this removes is cost. Reintroducing it would defeat the point.

---

## License

Released under CC BY 4.0. Use it in your classroom, your workshop, your program. Modify it, translate it, rebuild it, fold it into your own curriculum, share it however you like. The only condition is attribution.

---

## Companion projects

**[4LS](https://slowcities.github.io/4LS/)** — a subtractive synthesizer you can see through, built on the same principles.

**[16Max](https://slowcities.github.io/16max/)** — a sixteen step sequencer with probability, ratchets and ties.

**[Video Surfer](https://slowcities.github.io/video-surfer/)** — a browser-based experimental video synthesizer in the Rutt/Etra lineage.
