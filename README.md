# Drum Evaluator

A real-time drum practice tool. Play along to a groove on an electronic kit
or drum pad, and it shows how close each hit landed: early, late, or right
on, as you play.

> **Status: early prototype, in active development.** The source code is
> private for now. This page is for following progress, the roadmap, and
> giving feedback.

![Drum Evaluator's Practice screen: a sidebar on the left (Practice,
Metronome, Groove Editor, History, Settings), the Flamacue rudiment as drum
notation with its flams' small slashed grace notes and the sticking (lR, L,
R, ...) printed under each note, a timeline row underneath, and one row of
controls along the bottom: Start, the groove, tempo, loops and
click](screenshots/2026-10-23-practice.png)

*The Practice screen, ready to play the Flamacue rudiment at 80 BPM. The
groove is shown as drum notation, with each flam's grace note just in front
of its main note and the sticking (which hand plays each note) printed
underneath. Below the music, the timeline gets a mark for every hit as you
play. Everything you need is along the bottom: Start, the groove, tempo,
loops and the click.*

## A new app (2026-10-23)

Drum Evaluator has been rebuilt from the ground up as one app for Windows,
Mac, iPhone/iPad and Android. Windows is finished; the others are next.

- **The same scores as before.** The same playing gets the same score as
  in the first version.
- **A steadier click.** On one setup, the click holds its timing to about
  a tenth of a millisecond (the first version's varied by 3-4 ms).
- **All new screens:** a sidebar with Practice, Metronome, Groove Editor,
  History and Settings, in light or dark.
- **Your kits, history and grooves come with you** from the first version.
  Each kit needs calibrating once more.

## What it does today

- **Play along to a pattern.** Load a groove (a standard `.mid` file,
  e.g. exported from Guitar Pro or a DAW), or one of the built-in grooves
  and rudiments, set the tempo and number of loops, and play along to a
  count-in (clicks or spoken) and click (off, beats, 8ths, triplets or
  16ths). Changing grooves keeps the tempo you've set. Any pattern works
  with any kit: drums your kit has no pad for are still shown but not
  scored, and Start tells you which ones.
- **Live feedback on every hit.** Each note is scored as you play: hit,
  missed, or extra, and graded from *tight* to *off* by how far from the
  beat it landed. The notes in the music turn the colour of how close you
  hit them, and the timeline underneath marks each hit where it landed,
  with its own shape for each grade.
- **Drum notation.** The groove as real sheet music: x noteheads for
  cymbals, ghost notes in parentheses, accents, flams, triplets,
  sextuplets, 32nds, quintuplets and septuplets, open hi-hats, and the
  sticking under the notes. The print size can be changed, and grooves
  longer than the screen move on as you play.
- **Rudiments.** The Rudiments tab lists the built-in rudiments: single,
  double and triple stroke rolls, the 5 to 17 stroke rolls, paradiddles
  and paradiddle-diddles, flams, flam accents, flam taps, flamacues,
  pataflaflas, Swiss Army triplets and more, each with its sticking.
- **Flams scored properly.** A flam's two notes are matched as a pair and
  timed by the main note. Inverse flams (the soft note just after the
  main one) are supported too. After playing, a flam's note says in each
  loop if its grace note came on the wrong side or was missed.
- **Fast playing.** Quick 16ths are matched in the order you play them:
  a run played consistently late is scored as late, not as misses. A
  pad's double-trigger (a faint second hit right after the first) is
  ignored.
- **Straight to the review.** When a session ends you see the score and
  stars, every note coloured by how it went over all the loops, and a
  one-line verdict. Tap a note to see each loop: how early or late, how
  loud, and its grade. "More" opens the full summary in plain words.
- **A score for every session.** 0-100 and 0-5 stars: mostly timing,
  plus volume for the drums you've asked it to check. Your personal best
  is kept for each groove at each tempo.
- **Dynamics.** Checks how evenly you play each note from loop to loop,
  and whether ghost notes stay quiet and accents stand out, judged against
  your own levels.
- **Steadiness judged per drum.** Each drum's timing is compared with its
  own average: a kick that's always a touch ahead of the hi-hat doesn't
  count against you.
- **History.** Every completed session is kept, with a chart of your
  scores on each groove. Open any past session to see its review again,
  this time with the exact figures.
- **Groove Editor.** Make and change grooves two ways, on one grid:
  - **Tap them in**: tap a cell for a hit, again for an accent, then a
    ghost note, a flam, an inverse flam, then empty. Each beat has its own
    grid: tap its number to choose 16ths, 32nds, triplets, sextuplets,
    quintuplets or septuplets. Set the length (1 to 4 bars), tempo and
    time signature.
  - **Sticking**: give each note a hand (R or L; a flam's grace its own
    hand), shown under the notes when you practise. Sticking isn't
    scored.
  - **Play them in**: press Record and keep repeating a groove of 1, 2 or
    4 bars. Every hit appears on the grid as you play, a thin lane per
    repetition, showing how early or late it was. The app works out the
    groove's length and keeps your usual dynamics, ready to tidy up and
    save.

  Built-in grooves are never changed: saving one keeps your version in
  Your grooves. You're asked before unsaved changes are lost, and before
  saving over one of your own grooves.
- **Standalone metronome.** Tap tempo, any time signature, 1 to 8 clicks
  per beat, swing, built-in patterns (odd meters ready-grouped, clave),
  tap a step to accent, soften or mute it, and a full-screen flash.
  Keyboard: Space starts and stops, Up/Down change the tempo, T taps it.
- **Polyrhythms.** Up to four click tracks at once (3 against 2, 5
  against 4, 4:3:2, ...), each with its own sound, pitch and volume.
- **Set up your pads by hitting them.** Press Learn and hit the pad; the
  screen says which drum in big letters, readable from the kit. Pads that
  send a different note for the rim can be given both. Add your own
  pieces (splash, china, cowbell, a second snare, ...).
- **Saved kits.** Keep several kits (say, a practice pad and a full
  e-kit), each with its own pads, tolerance and calibration, and switch
  between them.
- **Latency calibration, three ways**, most accurate first:
  - **Microphone**: a mic near the pad measures your setup's delay itself
    (about ±10 ms), in about 15 seconds.
  - **Tap along** to the click: join in when you're ready; a short
    warm-up, then 8 beats are measured, and it only saves once two takes
    agree.
  - **Your kit's own metronome**: play along to it instead; the app lines
    its grid up with your playing afterwards.

  If you switch to a different audio output, the app reminds you to
  calibrate again.
- **Shares your audio.** Play music or a lesson video alongside it, or
  record your screen with sound.
- **Runs entirely on your computer.** No account, no internet connection,
  nothing uploaded.

![The review screen after a session: a score of 93 with four stars and "On
the beat · fairly steady" at the top, a one-bar groove in notation with
each note coloured by how it went, a popup on one open hi-hat note listing
its four loops (tight, good, tight, tight, and how many ms early), and the
timeline underneath with a shape for each hit](screenshots/2026-10-23-review.png)

*A session's review, opened from History: 93 and four stars. Each note is
coloured by how it went over the four loops (green: tight, teal: good).
Tapping the open hi-hat on "1-and" shows every loop: all within 10 ms,
slightly early.*

![The Groove Editor with the Swiss Army Triplet rudiment: a grid with a row
per drum, the snare's notes showing their sticking (rL, L, R), and the grid
menu open for beat 1: 16ths, 32nds, triplets (selected), sextuplets,
quintuplets and septuplets, those the beat's notes wouldn't fit greyed
out](screenshots/2026-10-23-groove-editor.png)

*The Groove Editor with the Swiss Army Triplet open. Tapping a beat's
number opens its grid menu: this beat is in triplets, and the grids its
notes wouldn't fit are greyed out. Each snare note shows its sticking; a
flam's is written with its grace note's hand first ("rL").*

![The metronome: 120 BPM in large numbers with tempo and Tap buttons and
Start, time signatures 3/4 to 7/8 plus Other, a swing slider, and in
polyrhythm mode two tracks: 4 beats with 2 clicks each, and 3 beats, each
step a box as tall as it is loud](screenshots/2026-10-23-metronome.png)

*The metronome playing 4 against 3: the main track in 4/4 with 8ths, the
second track's three evenly spaced beats underneath. Each step is as wide
as it lasts and as tall as it's loud: tap one to accent, soften or mute
it.*

![The groove picker on the Rudiments tab: Single Stroke Roll, Four Stroke
Roll, Triple Stroke Roll, Quads, Double Stroke Roll, 5, 6 and 7 Stroke
Roll, each 4/4, 1 bar](screenshots/2026-10-23-rudiments.png)

*Choosing a groove: built-in grooves, rudiments and your own.*

**Works with:** Windows today, plus any electronic kit or drum pad that
sends MIDI over USB. Mac, iPhone/iPad and Android versions are next.

## Coming to phones

The phone screens are laid out for every size from the small iPhone SE to
the largest Pro Max (pictures in the 2026-10-16 changelog). On a phone:

- **Practise with the phone sideways on a stand**, every button big enough
  to tap from the kit.
- **The Groove Editor and recording go sideways too.**
- **The metronome works upright or sideways.**
- **Light and dark**, following your phone's own setting.

## Roadmap

**Next up**
- **Mac**, then **iPhone/iPad** and **Android**, with the same scoring
  on every platform, and flams drawn clearly in the notation on small
  screens.
- **A test version to share**: an installable Windows app for a few
  testers to try.
- **Easier setup for pads that send two notes** (e.g. one for soft hits,
  one for hard).
- **Simpler calibration instructions.**

**Practice and progress**
- **Hear a pattern**: play a groove or rudiment back before you try it.
- **History overview**: across all your grooves, which ones and which
  drums are weakest, and what's improving.
- **Play back past sessions**: listen to what you played, optionally with
  the click over it.
- **Tempo trainer**, two ways: change the tempo by a set amount every few
  bars, or go up only once you've played accurately enough for a while.
- Practicing time-signature changes (e.g. 4 bars of 4/4, then 2 of 7/8).

**Metronome and click**
- Save your own click patterns, with several bars and meter changes, and
  use them during scored practice too.
- Gap click: the click drops out for a few bars, then comes back.
- Click that follows the pattern: the click sounds on the groove's own
  notes, or only on notes you pick.
- The metronome's finer subdivisions (sextuplets, 32nds, quintuplets,
  ...) during scored practice too.
- Tempo counted in dotted quarters for 6/8 and 12/8.

**Groove Editor**
- The groove as notation in the editor too.
- A score for your recordings, like the one for play-along sessions.
- Recording finds 3-bar grooves, and optionally you tell it the length
  before you start; the length worked out from all the bars played.

**Patterns**
- The drag rudiments (drags, ratamacues, Lesson 25, ...), with a drag's
  two grace notes shown and scored.
- A library of common grooves by genre.

**Later**
- Acoustic drums via microphones.
- An About screen crediting every open-source library and font the app
  uses, then polished, installable apps for all four platforms.

See [CHANGELOG.md](CHANGELOG.md) for what's changed recently.

## Feedback

Ideas and feature requests are welcome. Open an issue on this repo.
