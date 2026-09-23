# research-archive

The research behind the projects on this account: what inspired each one, the references it was measured against, what was learned while building it, and why the technical choices were made.

## Layout

```
projects/<repo-name>.md   one file per project, named after its repository
topics/                   research that spans several projects
TEMPLATE.md               the section layout for a new project file
```

Each project file has the same sections:

- **Inspiration** - the reference, competitor or brief that started it
- **References** - links and sources, with what each one contributed
- **Findings** - what was learned by comparing against the reference and testing
- **Technical decisions** - the choice and the reason for it
- **Gaps** - research known to exist but not yet written up here, with where and when it happened

## Projects

| Project | Started from |
| --- | --- |
| [ISSEN](projects/issen.md) | An X post by the developer sensonoken showing a production Unity sword-duel game with a sumi-e ink look. |
| [FRAME ZERO](projects/frame-zero.md) | An original production brief from the owner (2026-09-19): an interactive animated manga whose pages control reality instead of depicting it. |
| [KESTREL-9](projects/kestrel-9.md) | Not recorded in the repos. |
| [Open Muse](projects/open-muse.md) | Meta's Muse agent concept: a personal agent that takes work off your plate. |
| [EDGE//AI](projects/edge-ai.md) | PocketPal and google-ai-edge/gallery (GitHub). |
| [O Empire](projects/o-empire-reborn.md) | The Steam game O EMPIRE! WARD OFF THY ROT. |
| [FrameForge Studio](projects/frameforge-studio.md) | Benchmarks named in the brief (2026-09-17): Adobe Premiere, DaVinci Resolve and CapCut. |
| [WILDLIGHT: Valley Run](projects/wildlight.md) | A forest-valley demo shown as made with Unreal / GPT Astra, sent by the owner on 2026-09-21. |
| [KIN](projects/kin-living-pond.md) | RYUKIN by Masataka Hakozaki (Google Play: https://play. |
| [Linefold](projects/linefold.md) | Mini Metro (Dinosaur Polo Club). |
| [Tidemill](projects/tidemill.md) | Townscaper (Oskar Stålberg). |
| [Tiny Patiala](projects/tiny-patiala.md) | An isometric miniature-city post on X (2026-09-21), made for the owner's own town, Patiala, Punjab. |
| [Patiala Flatball](projects/patiala-flatball.md) | The Flatball illustration style (a painted world wrapped around a sphere), from an X post on 2026-09-21. |
| [Tide, remembered](projects/ukiyo-tide.md) | Edo-period ukiyo-e woodblock prints, in particular the great-wave composition. |
| [NoCatch](projects/nocatch.md) | There's An AI For That (TAAFT), as a free and serious alternative. |
| [Sift](projects/sift.md) | Bouncer by Imbue (Play Store listing sent 2026-09-22). |
| [Stillwater](projects/stillwater-harbor.md) | A night-sailing render presented as made with GPT Astra (sent 2026-09-21). |
| [Clock Out](projects/clock-out.md) | An office stealth game shown in an X post: https://x. |
| [GAZESCOPE](projects/gazescope.md) | Owner brief (2026-09-20): an AR eye tracker. |

## Adding research

- New research on an existing project goes into that project's file, under the matching section, with a date when it matters.
- A new project gets a new file copied from [TEMPLATE.md](TEMPLATE.md).
- Research that applies to several projects (rendering techniques, local-first security, mobile performance) goes in `topics/`, linked from each project that uses it.
- Link the original source wherever one exists. If a finding came from testing, say what was tested.

## About the gaps

Some of the research behind these projects happened in conversation and never reached a repository. Rather than reconstruct it from memory, each project file lists those topics under **Gaps** with a date so they can be written up properly later. Everything else here comes from the project repositories and dated project notes.

## Related

Part of a set of three: this repo is the research, [plan-orchestrator](https://github.com/aeiouvcode/plan-orchestrator) is the working method (agent contract, state templates, orchestration rules), and [agent-specific-notes](https://github.com/aeiouvcode/agent-specific-notes) is the failure log.
