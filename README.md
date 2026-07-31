# clapboardbench

Real-robot eval traces: a bimanual YAM arm rig operating a film
clapperboard, driven turn by turn by frontier vision-language models.
Each run captures everything the model saw and did: the camera frames it
was sent, its per-move reasoning notes, every tool call, joint states,
videos, and the raw API wire traffic.

The task: "Lift the clapper stick, then let go so it snaps shut with a
clap." Models under test: `claude-opus-5` and
`gemini-robotics-er-2-preview`, each controlling both 6-DoF arms and
grippers through the same tool interface, one motion per LLM call.

## Read the runs (start here)

Open **[2026-07-31/runs/](2026-07-31/runs/)**. GitHub renders the index
table directly: 11 runs labeled `gemini-1` to `gemini-5`, `opus-1` to
`opus-5` (chronological within each model), and `opus-early`, with
outcome, steps, and duration. Each run page shows:

- a metadata header (model, effort, outcome, operator judgement, timing),
- every observation expanded in place: joint states plus the exact
  224x224 camera frames the model received at that step,
- the full turn-by-turn transcript: the model's note and tool call for
  every motion, with the system prompt collapsed behind a click,
- links to per-camera MP4s of the whole run, playable in the browser.

## What is in a run

| What | Where |
|------|-------|
| EvalLog (config, results, embedded transcript) | `2026-07-31/adhoc_*.json` |
| Per-trial message transcript | `2026-07-31/transcripts/<stamp>/scene-*.jsonl` |
| Raw API wire capture, images deduplicated as content-addressed blobs | `2026-07-31/wire/<stamp>/` |
| Camera videos (one MP4 per trial and camera) | `2026-07-31/videos/<stamp>/` |

Runs are cross-referenced by `<stamp>` (the basename of each log's
`stats.frames_dir`). The markdown pages are deterministic renders of
these raw files; images on the pages link straight into the wire blobs.

## Provenance

Captured 2026-07-30 and 2026-07-31 on a real dual-arm rig, selected
from a larger internal 24-hour capture window. Outcomes were judged
live by a human operator (`pass`, `fail`, `partial`); runs the operator
did not judge carry their raw status. The EvalLog format is
inspect-robots; the page renderer is internal tooling.
