# Data disclaimer

## Physiological data is synthetic

Every heart-rate figure in this repository is generated. That includes
`configs/roster/session01.yaml`, `reports/sample_match/physio.json`,
`reports/sample_match/physio_timeline.csv`, the `mean_hr_bpm` / `max_hr_bpm` /
`trimp` columns of `reports/sample_match/players_summary.csv`, and the
cardiac panels of `reports/sample_match/match_report.html`.

The roster uses the names of real, well-known footballers as recognisable
placeholders so the schema reads naturally. **No real athlete was recorded, no
real strap data was collected from any named person, and none of the resting
heart rates, maximum heart rates, HR-zone distributions, TRIMP scores or
cardiac-lag figures describe a real individual.** They are illustrative values
that exercise the Polar ingestion, synchronisation and fusion code paths.

Disclosure is carried by the files themselves, not only by this document. The
roster and the JSON exports are tagged in-band with
`data_classification: "SYNTHETIC"`, and the sample HTML report renders a banner
saying so. The CSV exports are deliberately left untagged so they still show the
exact schema a coach receives; they are documented instead in
[`reports/sample_match/README.md`](../reports/sample_match/README.md).

## What is measured, not synthetic

The camera and computer-vision results are real measurements taken on real
hardware, and are reproducible with the commands recorded beside them in
`FINDINGS.md`:

- Lens intrinsics and extrinsics calibration RMS values.
- Detection, tracking, homography and overlay throughput benchmarks.
- The free-gravity ballistic audit that recovers -9.89 m/s^2.
- Pose and OCR latency figures.

## Match footage

The football, American football and basketball clips used to produce the demo
media in `reports/demos/` are owned or licensed by the repository author.
