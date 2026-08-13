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

Open **[2026-07-31/runs-html/](2026-07-31/runs-html/)**, download a run
page, and open it in a browser (GitHub does not render HTML in place;
`index.html` is the run index). The 11 runs are labeled `gemini-1` to
`gemini-5`, `opus-1` to `opus-5` (chronological within each model), and
`opus-early`. Each page is a single self-contained file rendered with
`inspect-robots view`:

- a metadata header (model, effort, outcome, operator judgement, timing),
- the full turn-by-turn transcript: the model's note and tool call for
  every motion, with the exact 224x224 camera frames and joint states
  the model received inline at each step,
- per-camera flipbook scrubbing and an embedded video of the whole run,
  synced to the transcript,
- the raw API wire capture rendered in place.

To read directly on GitHub without downloading anything, the same runs
are rendered as markdown in [2026-07-31/runs/](2026-07-31/runs/), with
an index table (outcome, steps, duration) and per-run pages. Rerun
recordings of every run live in [2026-07-31/rrd/](2026-07-31/rrd/) —
camera streams, joint-position series, and the transcript on the step
timeline; view with `rerun <file>.rrd` or at
[rerun.io/viewer](https://rerun.io/viewer), and see
[rrd/README.md](2026-07-31/rrd/README.md) for the per-run index.

## What is in a run

| What | Where |
|------|-------|
| EvalLog (config, results, embedded transcript) | `2026-07-31/adhoc_*.json` |
| Per-trial message transcript | `2026-07-31/transcripts/<stamp>/scene-*.jsonl` |
| Raw API wire capture, images deduplicated as content-addressed blobs | `2026-07-31/wire/<stamp>/` |
| Camera videos (one MP4 per trial and camera) | `2026-07-31/videos/<stamp>/` |
| Self-contained HTML report (`inspect-robots view`) | `2026-07-31/runs-html/<run>.html` |
| Rerun recording (rebuilt offline from the capture) | `2026-07-31/rrd/<run>.rrd` |

Runs are cross-referenced by `<stamp>` (the basename of each log's
`stats.frames_dir`). The markdown pages are deterministic renders of
these raw files; images on the pages link straight into the wire blobs.

## Provenance

Captured 2026-07-30 and 2026-07-31 on a real dual-arm rig, selected
from a larger internal 24-hour capture window. Outcomes were judged
live by a human operator (`pass`, `fail`, `partial`); runs the operator
did not judge carry their raw status. The EvalLog format is
inspect-robots; the page renderer is internal tooling.
