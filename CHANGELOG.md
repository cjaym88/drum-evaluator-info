# Changelog

Notable changes to Drum Evaluator, newest first.

## 2026-10-05

![The standalone metronome in 7/8, grouped 2+2+3](screenshots/2026-10-05-metronome.png)

- **Standalone metronome.** A full metronome that works on its own, no
  kit needed. Set the tempo with buttons, a slider, the arrow keys or tap
  tempo. Use any time signature, add subdivisions from 8ths to
  quintuplets and sextuplets, and dial in swing from 0% (straight) to
  100%.
- **Built-in click patterns.** 2/4 through 13/8 (odd meters ready-grouped,
  e.g. 7/8 as 2+2+3 or 3+2+2), swing 8ths and 16ths,
  son, rumba and bossa nova clave, and 3:2, 4:3 and 2:3 polyrhythms.
- **Edit the click step by step.** Click any step to make it an accent,
  normal, soft or silent. Your accents stay when you change the
  subdivision. Tempo and step changes are heard right away;
  a new time signature starts at the next bar line.
- **Scoring checked against research.** The timing grades and the words
  in the summary were compared with published studies of drummers'
  timing. The current thresholds hold up: for example, "very steady"
  matches the consistency of professional drummers. The comparison also
  found two improvements now on the roadmap: judging each drum's
  steadiness against its own feel (pros naturally play kick and snare a
  touch ahead of the hi-hat), and fewer false misses at fast tempos.
- **Plans for Mac, iPhone/iPad and Android.** The app is being organized
  so one shared scoring engine runs on all four platforms, so the same
  playing gets the same score everywhere.
- **Known issue:** while the click plays, other apps can't use the same
  sound output (no music or lesson videos alongside). A fix is being
  worked on.

## 2026-10-01

![The app on 2026-10-01](screenshots/2026-10-01.png)

- **Dynamics feedback.** How evenly each note of the groove is played
  across loops, compared only with its own repeats (the snare on 2 with
  other snares on 2), and whether ghost notes stay quiet and accents stand
  out. Shown live under each note on the timeline.
- **Works with any velocity curve.** Pads offer different curves for
  turning hit strength into volume. Dynamics are judged in a way that gives
  the same answer whichever curve your pad uses.
- **Plain-language summary.** Results now read like a teacher's notes:
  how it went, timing in words, uneven notes by where they fall in the bar
  ("snare ghost note on 2-a"), and one "Try next" suggestion. The detailed
  numbers are behind a **Show details** button.
- **Volume feedback per drum.** A checkbox on each drum's row turns its
  volume feedback on or off. Cymbals start off, since their volume rarely
  matters and would clutter the feedback.
- **New click engine.** The metronome now plays directly through the sound
  card, timed to the exact sample. The click's own delay is compensated
  automatically, so calibration only has to measure the player and the pad.
- **Clearer calibration.** Calibration only sounds the clicks you're meant
  to hit. Extra in-between clicks made it easy to follow the wrong ones.
- Timing that's *off* now shows in red in the timeline.
- Fixes in free-play loop detection and in re-scoring saved recordings.

## 2026-09-30

![The app on 2026-09-30](screenshots/2026-09-30.png)

- **Desktop app.** Pick a pattern, tempo and loops, then watch each hit
  land on a live timeline, with a summary at the end. A pattern preview
  shows when you select one.
- **Calibration in the app**: hit any one pad along with the click. Several
  takes are combined so one off take can't skew the result.
- **First successful live run**: every note of a syncopated groove with
  ghost notes was detected and scored on a real drum pad.
- Play-along sessions with live scoring, a count-in, and an adjustable
  click (beats, 8ths, triplets, 16ths).
