# Runs: 2026-07-31

One markdown page per eval run, generated from the adhoc_*.json
EvalLogs by analysis/render_runs_md.py. Each row links to the run
page; video links open MP4s that GitHub plays in the browser.
Runs are labeled gemini-1 to 5 and opus-1 to 5 in chronological
order; opus-early is the earlier operator-judged pass.
Run pages embed the camera frames the model saw, resolved from
the wire captures, for runs whose capture holds frames.

Dataset layout and provenance: [../README.md](../README.md).

| Run | Model | Instruction | Outcome | Steps | Duration | Video | Log |
|---|---|---|---|---|---|---|---|
| [gemini-1](gemini-1.md) | gemini-robotics-er-2 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 81 | 02:04 | [top](../videos/20260731_032044_1aa85267/scene-0-e0_top_cam.mp4) | [json](../adhoc_b933500d.json) |
| [gemini-2](gemini-2.md) | gemini-robotics-er-2 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 112 | 03:22 | [top](../videos/20260731_032325_b30d365b/scene-0-e0_top_cam.mp4) | [json](../adhoc_adbf4094.json) |
| [gemini-3](gemini-3.md) | gemini-robotics-er-2 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 180 | 04:40 | [top](../videos/20260731_032709_ac526471/scene-0-e0_top_cam.mp4) | [json](../adhoc_99f00f7a.json) |
| [gemini-4](gemini-4.md) | gemini-robotics-er-2 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | error | 136 | 04:30 | [top](../videos/20260731_033158_b6701524/scene-0-e0_top_cam.mp4) | [json](../adhoc_f9fbd43b.json) |
| [gemini-5](gemini-5.md) | gemini-robotics-er-2 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 55 | 00:48 | [top](../videos/20260731_033801_60509b7b/scene-0-e0_top_cam.mp4) | [json](../adhoc_ab9d2a7d.json) |
| [opus-1](opus-1.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | pass | 143 | 04:48 | [top](../videos/20260731_021816_12f6942f/scene-0-e0_top_cam.mp4) | [json](../adhoc_8ba42f7e.json) |
| [opus-2](opus-2.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 188 | 04:39 | [top](../videos/20260731_022331_512a92a8/scene-0-e0_top_cam.mp4) | [json](../adhoc_1852de3c.json) |
| [opus-3](opus-3.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 1235 | 29:03 | [top](../videos/20260731_022834_cf776563/scene-0-e0_top_cam.mp4) | [json](../adhoc_f01e3de3.json) |
| [opus-4](opus-4.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 218 | 08:10 | [top](../videos/20260731_025950_0725a03f/scene-0-e0_top_cam.mp4) | [json](../adhoc_6369aa14.json) |
| [opus-5](opus-5.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | fail | 233 | 07:50 | [top](../videos/20260731_030913_998e7330/scene-0-e0_top_cam.mp4) | [json](../adhoc_c5a86c6b.json) |
| [opus-early](opus-early.md) | claude-opus-5 | Lift the clapper stick, then let go so it snaps shut with a clap. Note... | pass | 559 | 17:21 | [top](../videos/20260731_005105_0cef4e6e/scene-0-e0_top_cam.mp4) | [json](../adhoc_00efecfc.json) |

11 runs: 11 with video, 11 with transcript jsonl, 11 with wire capture.
