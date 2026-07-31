# 2026-07-31

Eleven eval runs with full per-run assets, all on the clapperboard task:
"Lift the clapper stick, then let go so it snaps shut with a clap."
Hand-picked from a 24-hour capture window on the rig, ending
2026-07-30 ~22:10 PDT.

Selection:

- gemini-1 to gemini-5: the 5 most recent Gemini runs
  (`gemini-robotics-er-2-preview`, 2026-07-31 03:20 to 03:38 UTC, in
  chronological order): `adhoc_b933500d`, `adhoc_adbf4094`,
  `adhoc_99f00f7a`, `adhoc_f9fbd43b` (errored), `adhoc_ab9d2a7d`.
- opus-1 to opus-5: Opus runs 2 through 6 counting back from the newest
  (`claude-opus-5`, 02:18 to 03:09 UTC, chronological): `adhoc_8ba42f7e`,
  `adhoc_1852de3c`, `adhoc_f01e3de3`, `adhoc_6369aa14`, `adhoc_c5a86c6b`.
- opus-early: `adhoc_00efecfc` (claude-opus-5, 00:51 UTC), the
  operator-judged pass.

Browse the runs as markdown in [runs/](runs/). Layout: `adhoc_*.json`
EvalLogs, `transcripts/<stamp>/`, `videos/<stamp>/`, `wire/<stamp>/`.
Files are verbatim copies from the full capture window, which is
retained internally.
