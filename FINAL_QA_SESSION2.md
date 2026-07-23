# Kretz Session 2 — Final Synchronization QA

## Status

The Session 2 package is synchronized across:

- `index.html`
- `kretz_prompting_session_2.html`
- `kretz_session_2_run_of_show.html`
- `kretz_prompting_session_2_deck.pptx`
- `kretz_prompting_session_2_handout.pdf`
- `kretz_prompt_to_tool_builder_example.html`
- `kretz_haul_costs_reference_workbook.xlsx`
- the Session 2 dataset folder and ZIP
- `kretz_session_2_sources_and_links.md`
- `README_SESSION2.txt`

## Corrections completed

- Removed references to private leadership conversations, personal requests, and implied technology decisions.
- Restored the strong employee behavior rules:
  - AI fills in what you leave blank.
  - AI is not a calculator.
  - AI cannot forecast lumber prices.
  - If a number cannot be traced to a source, do not use it.
  - A person signs off.
- Corrected the homepage prototype count to `5 + 2`.
- Separated Session 1 materials from Session 2 materials and removed duplicate/versioned participant labels.
- Relabeled the ten-step flow as Session 1.
- Replaced the paywalled Zillow link with Zillow’s official investor release.
- Updated Wisconsin parcel notes to the V12/2026 training reference and added appropriate-use boundaries.
- Corrected the synthetic price-data wording: red-herring correlations round to `0.00`; they are not claimed to be exactly zero.
- Renamed `driver_hours` to `driving_hours` in the haul-cost practice file and workbook.
- Reframed the 11-hour workbook value as a training screening threshold, not a complete compliance determination.
- Replaced real-looking participant initials in the Timber Sale Tracker with fictional labels `F1`, `F2`, and `F3`.
- Fixed local-date handling in the Timber Sale Tracker.
- Fixed timer pause/restart behavior in the facilitator run-of-show.
- Rebuilt the PowerPoint and handout to match the final eight-activity flow.
- Removed nested-ZIP upload instructions. The final upload ZIP extracts directly into the repository root.

## Validation completed

- PowerPoint: 30 slides; rendered and visually reviewed; slide overflow test passed.
- PowerPoint: overlap and out-of-bounds diagnostics passed without warnings.
- Handout: 6 pages; rendered and visually reviewed.
- Workbook: 5 printed pages after print-setting cleanup.
- Workbook: 482 formulas; no cached formula errors found after recalculation.
- HTML: inline JavaScript syntax checked with Node.
- HTML: duplicate IDs and local links checked.
- Dataset folder and dataset ZIP rebuilt from the same corrected files.

## Existing repository dependencies

These three prototype files are linked by the portal and should remain in the repository root:

- `Claude_Parcel.html`
- `kretz-landowner-prospecting.html`
- `kretz-haul-planner.html`

They were already present in the project screenshot but were not included in the latest Session 2 upload supplied for this update.

## Current official references used

- Wisconsin statewide parcel data V12: https://www.sco.wisc.edu/parcels/data/
- Wisconsin county parcel downloads: https://www.sco.wisc.edu/parcels/data-county/
- Wisconsin Managed Forest Law: https://dnr.wisconsin.gov/topic/forestlandowners/mfl
- FMCSA hours-of-service summary: https://www.fmcsa.dot.gov/regulations/hours-service/summary-hours-service-regulations
- Zillow Offers wind-down release: https://investors.zillowgroup.com/news-and-events/news/news-details/2021/Zillow-Group-Reports-Third-Quarter-2021-Financial-Results--Shares-Plan-to-Wind-Down-Zillow-Offers-Operations/default.aspx
