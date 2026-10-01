# Drum Evaluator

A real-time drum practice tool. Play along to a groove on an electronic kit
or drum pad, and it shows how close each hit landed: early, late, or right
on, as you play.

> **Status: early prototype, in active development.** The source code is
> private for now. This page is for following progress, the roadmap, and
> giving feedback.

![Drum Evaluator after a play-along session: a timeline with a row per drum,
each hit shown as a colored dot inside its timing window, and a session
summary below](screenshots/2026-10-01.png)

*After a 4-loop session on a syncopated groove: each dot is one hit, placed
left or right of the beat by how early or late it was, and colored by how
close it landed.*

## What it does today

- **Play along to a pattern.** Load a groove (a standard `.mid` file,
  e.g. exported from Guitar Pro or a DAW), set the tempo and number of loops,
  and play along to a count-in and click.
- **Live feedback on every hit.** Each note is scored as you play: hit,
  missed, or extra. Hits are graded from *tight* to *off* by how far from
  the beat they landed, in milliseconds.
- **Timeline view.** A one-bar timeline with a row per drum shows where
  each hit landed against where it should have, loop by loop.
- **Ghost notes.** Quiet and loud notes are told apart, so dynamics in a
  groove are kept.
- **Latency calibration.** A short "hit any pad along with the click" test
  measures your setup's delay, so on-time playing scores as on time.
- **Sample-accurate click.** The metronome is played directly through your
  sound card and placed to the exact sample.
- **Session summary.** Totals, average timing, and how early or late you
  tend to play per drum, saved after each session.
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
