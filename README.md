# Project Zomboid Watch UI CPU study

Recorded data from the 2026-10-30 controlled comparison for Project Zomboid B42.22: 52 scenarios, five full-day repetitions each, 260 measurements and 105,300,000 scheduled display calls. Each sample covers a 5,400-second timeline at 30 or 120 scheduled UI calls per second.

This measures selected watch display/update paths using the installed Java/Kahlua runtime, including the replay driver and command observer. It does not measure an entire game session, native equipment searches, background callbacks, the actual rendering queue or GPU. Displays have different features; the results do not establish code-quality rankings or feature-equivalent efficiency.

Commissioned by Antikristianos, developer of Hi-Res Clock. GPT via Codex developed and operated the benchmark tools, analyzed the recorded measurements and prepared the study. The commissioner specified scope and reviewed presentation; he did not modify measurements or calculated results or specify a preferred ranking. This attribution is not independent validation of the method.

## Data

- [Download the complete evidence ZIP](./watch-cpu-evidence-2026-10-30.zip?raw=1)
- [Raw recorded samples](./raw.csv)
- [Derived statistics](./analysis.csv)
- [All scenarios and observed variation](./All%20scenarios.md)

The ZIP includes the study's method/scope notes, original input hashes, case order, individual JVM logs, metadata, observed timing variation, release-equivalence evidence and artifact checksums. Original source paths are retained in the measurement records. Game files and third-party mod source/assets are not redistributed.

All 260 samples completed. The original launcher's broad input guard stopped because an unselected duplicate directory disappeared. The retained audit documents that every potentially used input remained unchanged and matches every raw record against its original log. Reconstructed metadata keeps the original guard failure explicit. Earlier invalid qualification figures are excluded from these results.

The technical CSV ratios compare Vanilla at the same UI cadence. The companion guide's percentage charts instead use one fixed reference: total timeline CPU work of Vanilla at 30 UI FPS = 100%, for both cadence selections. Observed min/max ranges are not confidence intervals; five repetitions within one JVM per scenario do not establish between-machine or between-process uncertainty.

Companion Steam guide: [UI Mods and Performance: a Controlled Watch UI Case Study](https://steamcommunity.com/sharedfiles/filedetails/?id=3830533978).

## Evidence archive SHA-256

`F6D30D704302277EE1F51FE8D98113EA3800136AD49F2B84F408324E036C861C`
