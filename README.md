# Drum Evaluator

A real-time drum practice tool. Play along to a groove on an electronic kit
or drum pad, and it shows how close each hit landed: early, late, or right
on, as you play.

> **Status: early prototype, in active development.** The source code is
> private for now. This page is for following progress, the roadmap, and
> giving feedback.

![Drum Evaluator after a play-along session: a timeline with a row per drum,
each hit shown as a colored dot inside its timing window, "even" or "uneven"
under each snare note, and a plain-language session summary below](screenshots/2026-10-01.png)

*After a 4-loop session on a syncopated groove: each dot is one hit, placed
left or right of the beat by how early or late it was, and colored by how
close it landed. Under each snare note: whether its volume stayed even
across the loops. Below: the session summary in plain words.*

## What it does today

- **Play along to a pattern.** Load a groove (a standard `.mid` file,
  e.g. exported from Guitar Pro or a DAW), set the tempo and number of loops,
  and play along to a count-in and click.
- **Live feedback on every hit.** Each note is scored as you play: hit,
  missed, or extra. Hits are graded from *tight* to *off* by how far from
  the beat they landed, in milliseconds.
- **Timeline view.** A one-bar timeline with a row per drum shows where
  each hit landed against where it should have, loop by loop.
- **Dynamics.** Checks how evenly you play each note of the groove from
  loop to loop, and whether your ghost notes stay quiet and your accents
  stand out. Each note is only compared with its own repeats, so a ghost
  note is judged as a ghost note and an accent as an accent. Works with any
  pad velocity curve, so you don't need to change your pad's settings.
  Volume feedback can be switched off per drum (cymbals start off).
- **Feedback in plain language.** After each session: how it went, your
  timing and each drum in words, which notes weren't even, and one thing to
  work on next. The full numbers are one click away.
- **Latency calibration.** A short "hit any pad along with the click" test
  measures your setup's delay, so on-time playing scores as on time.
- **Sample-accurate click.** The metronome is played directly through your
  sound card and placed to the exact sample.
- **Session history.** Every session's results are saved.
- **Runs entirely on your computer.** No account, no internet connection,
  nothing uploaded.

**Works with:** Windows, plus any electronic kit or drum pad that sends MIDI
over USB.

## Roadmap

Plans, not promises. Order and scope may change.

**Next up**
- **Standalone metronome**: a full metronome you can use on its own, no
  scoring needed.
- **Custom click patterns**: build your own click (which steps sound,
  accents, meter changes), and use it during scored practice too.
- **Click that follows the pattern**: an option for the click to sound on
  the groove's own notes instead of a fixed grid.
- **Pad "learn" mode**: hit a pad to assign it to a drum, no settings files.
- **Saved kits**: switch between kits (e.g. a practice pad and a full
  e-kit), each remembering its own setup and calibration.

**Practice and scoring**
- A single 0–100 accuracy score per session and per drum.
- Free-play mode: just play, and the app learns your groove and scores how
  consistent you are, with no pattern needed.
- Practicing time-signature changes (e.g. 4 bars of 4/4, then 2 of 7/8).
- Remembering your last pattern and settings.

**Patterns**
- A built-in groove editor.
- Rudiments (rolls, paradiddles, flams, ...).
- A library of common grooves by genre.

**Display**
- Standard drum notation alongside the timeline.
- Light and dark mode.
- Simpler, more guided calibration.

**Later**
- Acoustic drums via microphones.
- A polished, installable app.

See [CHANGELOG.md](CHANGELOG.md) for what's changed recently.

## Feedback

Ideas and feature requests are welcome. Open an issue on this repo.
