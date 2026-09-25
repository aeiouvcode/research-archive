# Aurelia

- Repository: https://github.com/aeiouvcode/aurelia
- Live: https://aeiouvcode.github.io/aurelia/

## Inspiration

Commissioned 2026-09-21 as "a hard task with little context": synthesize Mozart's Requiem Lacrimosa from a YouTube source - explicitly not a MIDI player and not a fetched MIDI file. Hard requirements: realtime in the browser, score displayed as it plays, downloadable audio of what was synthesized, and generalizable - "make this as a generalist engine to whom which i can tell any song from from the, and it can synthesize and play that song". "Do not cheat."

## References

- A doodlestein Codex/Bach post the owner flagged "Could help with aurelis" (2026-09-23), which drove the written-score-first rebuild. Exact URL in chat history.

## Findings

- Self-graded 4/10 against the real recording: oscillator voices cannot pass for human ones, and the first realization was a condensed ~3:00 rather than the full score.
- The rebuilt path composes the score first, never downloads one: engraved score with notes lighting as they play, sampled instruments. Live 2026-09-23, graded PARTIAL - choir weakest.
- Audio is dead inside a sandboxed preview page (CSP blocks inline Web Audio), so the preview is only a launcher; the working build is the GitHub Pages deploy.

## Technical decisions

- WebAudio physical/additive synthesis (strings, formant choir, winds, brass, timpani, hall reverb) with a live SATB score view.
- First original score delivered as a 2:48 short film, "Ember".

## Gaps

- The generalized "any song in, synthesis out" engine is the unsolved core; current state is composed scores rendered by the synth engine.
