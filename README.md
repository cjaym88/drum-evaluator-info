# Drum Evaluator

A real-time drum practice tool. Play along to a groove on an electronic kit
or drum pad, and it shows how close each hit landed: early, late, or right
on, as you play.

> **Status: early prototype, in active development.** The source code is
> private for now. This page is for following progress, the roadmap, and
> giving feedback.

![Drum Evaluator after a play-along session: the kit picker, a timeline with
a row per drum and up/down arrows to reorder them, each hit shown as a colored
dot inside its timing window, "even" or "uneven" under each snare note, and a
plain-language session summary below](screenshots/2026-10-07-main.png)

*After a 4-loop session on a syncopated groove: each dot is one hit, placed
left or right of the beat by how early or late it was, and colored by how
close it landed. Under each snare note: whether its volume stayed even
across the loops. Below: the session summary in plain words. The kit
picker (top left) switches between saved kits; the arrows next to each
drum reorder the rows.*

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
- **Set up your pads by hitting them.** In the Pads window, press Learn
  next to a drum and hit the pad: done, no settings files. Pads that send
  a different note for the rim or a hard hit can be given both. Add your
  own pieces (splash, china, cowbell, a second snare, ...) from a list or
  by name.
- **Saved kits.** Name and keep several kits (say, a practice pad and a
  full e-kit), each with its own pads and calibration, and switch between
  them from the main window: no recalibrating when you switch back.
- **Latency calibration.** A short "hit any pad along with the click" test
  measures your setup's delay, so on-time playing scores as on time.
- **Sample-accurate click that shares your audio.** Play music or a
  lesson video alongside it, or record your screen with sound.
- **Standalone metronome.** Use it on its own, no kit needed: tap tempo,
  any time signature, subdivisions, swing (0-100%), and built-in
  patterns from 2/4 to 13/8 (odd meters ready-grouped, e.g. 7/8 as
  2+2+3 or 3+2+2), and clave. Click any step to accent it, soften it or
  mute it. Every sound can be pitched up or down.
- **Polyrhythms.** Up to four click tracks at once (3 against 2, 5
  against 4, 4:3:2, ...), each with its own sound, pitch and volume.
- **Pattern detector.** No pattern file needed: play a groove of 1 to 4
  bars to the click and keep repeating it. The app works out how long it
  is, plots every hit on it as you play, and scores how steadily you
  repeat your own groove, so a laid-back or pushed feel counts as long
  as it's consistent. Then **save it as a pattern** to play along to
  later: fills and stray hits are left out, and your usual dynamics kept.
- **Room for big kits.** The windows resize, the grids scroll, and you
  can reorder the drum rows to suit how you read them.
- **Session history.** Every session's results are saved.
- **Runs entirely on your computer.** No account, no internet connection,
  nothing uploaded.

![The metronome in polyrhythm mode: a 4:3:2 polyrhythm, one row of steps
per click track, with the steps being heard lit up](screenshots/2026-10-05-polyrhythm.png)

*The metronome playing a 4:3:2 polyrhythm: the main track's 2 beats,
against 3 and 4 evenly spaced pulses on two more tracks, each with its
own sound. Taller boxes are louder; white boxes are the clicks being
heard.*

![The pattern detector after a session: a 2-bar groove found with confidence 1.00,
the drums played listed first with every hit plotted on a grid of the pattern,
pieces without a pad dimmed below, a Save as pattern button, and the
plain-language summary below](screenshots/2026-10-07-pattern-detector.png)

*The pattern detector after a 2-bar groove: hi-hat 8ths, kick on 1 and 3,
snare on 2 and 4, and a tom fill to end the second bar. It found the
2-bar length with full confidence. The drums you played move to the top;
each repetition is one thin lane; a dot's distance from its line is how
early or late it was against the click, and its color is how closely it
matched your own usual timing for that note (grey while a note is still
being learned). "Save as pattern..." keeps the groove for play-along.*

![The Pads window: every drum with its note numbers, Learn and Clear buttons,
custom pieces (Splash, Cowbell, Tambourine) with Remove buttons, the last pad
hit, and the kit picker at the top](screenshots/2026-10-07-pads.png)

*The Pads window, editing a full kit: hit a pad after pressing Learn to
assign it. "Last hit" shows what any pad is set to (here, the cowbell).
The kit picker at the top chooses which kit to edit, separately from the
kit you play with.*

**Works with:** Windows today, plus any electronic kit or drum pad that
sends MIDI over USB. Mac, iPhone/iPad and Android versions are planned.

## Roadmap

Plans, not promises. Order and scope may change.

**Next up**
- **Sharper scoring**: fewer false misses at fast tempos, steadiness
  judged per drum against its own feel, and more reliable calibration.
- **A single 0–100 accuracy score** per session and per drum.
- **Steadier pattern detection**: judge the pattern's length from all the
  bars played, so one varied bar can't change the answer.
- **Easier setup for pads that send two notes** (e.g. one for soft hits,
  one for hard), so none of their hits go missing.

**Metronome and click**
- Save your own click patterns (including each track's sounds), with
  several bars and meter changes, and use them during scored practice too.
- Tempo trainer, two ways: change the tempo by a set amount every few
  bars (up to build speed, or down to slow a fast passage), or go up
  only once you've played accurately enough for a while.
- Gap click: the click drops out for a few bars to test your inner time.
- Click that follows the pattern: an option for the click to sound on
  the groove's own notes instead of a fixed grid, or only on notes you
  pick.
- The metronome's finer subdivisions (16th-note triplets, 32nds,
  quintuplets, ...) during scored practice too.
- Tempo counted in dotted quarters for 6/8 and 12/8.

**Pattern detector**
- 3-bar patterns (today it finds 1, 2 and 4 bars).
- Optionally tell it the pattern's length before you start.
- Edit a saved groove in the groove editor.

**Practice and progress**
- **History view**: your progress on each pattern over time, plus an
  overview across all of them -- which grooves and drums are weakest,
  and what's improving.
- **Play back past sessions**: listen to what you played, optionally
  with the click over it, to hear where you rushed or dragged.
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

**Platforms**
- Mac, iPhone/iPad and Android versions alongside Windows, all sharing
  one scoring engine, so the same playing gets the same score everywhere.

**Later**
- Acoustic drums via microphones.
- Polished, installable apps for all four platforms.

See [CHANGELOG.md](CHANGELOG.md) for what's changed recently.

## Feedback

Ideas and feature requests are welcome. Open an issue on this repo.
