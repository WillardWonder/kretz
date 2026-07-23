# Kretz AI Training — Session 2 Sources and Links

Facilitator reference. Verify the Wisconsin data links during your dry run the
week of the session — portal versions and layer names change between releases.

---

## Wisconsin public land data (Activity 5)

These are the sources the model should surface in Shots 1–3. If it names
something else, click it before accepting it.

**Wisconsin Statewide Parcel Map Initiative**
Current training reference: **V12**, published in 2026. The statewide page says source parcel data was collected from counties in the first half of 2026 and most tax-roll records are from 2025. County and municipal records remain the current authority.

Aggregated annually from all 72 counties by the Department of Administration
with the State Cartographer's Office at UW–Madison. Free. Attributes include
owner name, mailing address, acreage, assessed values, property class, parcel
ID, and a point centroid.

- County-by-county downloads — https://www.sco.wisc.edu/parcels/data-county/
- Statewide parcel web viewer — https://maps.sco.wisc.edu/Parcels/

**Wisconsin DNR GIS / open data**
Forestry layers, including Managed Forest Law spatial data, moved onto the
DNR's open data portal.

- DNR GIS data landing page — https://dnr.wisconsin.gov/maps/GetGISData
- DNR Open Data portal — https://data-wi-dnr.opendata.arcgis.com

**Property class codes.** Wisconsin assessment classes under s. 70.32(2)(a) are
what let you filter to forest land. Class 5m is agricultural forest and class 6
is productive forest land — those two plus an acreage floor are the practical
filter for Shot 2.

**Managed Forest Law thresholds** (verified against the DNR program page):
enrollment is open to all private owners of forested land. A parcel must be at
least 20 contiguous acres under the same ownership, OR at least 10 contiguous
acres connected by a tract under the same ownership to another parcel of at
least 10 contiguous acres. At least 80% of each parcel must be productive
forest. An application requires a management plan written by a certified plan
writer.

Useful detail for the room:
- Orders run 25 or 50 years.
- Land is designated open or closed to public recreation; closed acreage costs
  more per acre and is capped per municipality.
- The 20-acre minimum rose from 10 acres in 2017, so older enrollments may look
  different from current rules.
- Forest Crop Law closed to new enrollment in 1986. FCL records in the practice
  file are legacy entries, which is realistic.

- MFL program page — https://dnr.wisconsin.gov/topic/forestlandowners/mfl
- MFL and timber sales — https://dnr.wisconsin.gov/topic/timbersales/mfl

### Caveats to state in the room

- Parcel data carries **mailing addresses, not email addresses.** This produces
  letters. Email addresses would have to come from existing customer records.
- The statewide layer is an **annual snapshot, not a live feed.** Ownership
  changes; the county remains the current authority.
- It is **not a survey** and establishes no legal boundaries.
- The statewide parcel data is publicly downloadable. Public availability does not make every outreach use appropriate. Follow approved practices, avoid protected or suppressed records, offer a respectful way to decline future contact, and require a human signature before anything goes out.
- Only the publicly published portions of MFL are spatially available. Do not
  assume full enrollment detail is mapped.

---

## AI News Break sources (carried from Session 1)

Four of these are reused in Session 2, each tied to a specific activity.

**Air Canada chatbot — you own what it says** (Activities 5, 8)
https://www.americanbar.org/groups/business_law/resources/business-law-today/2024-february/bc-tribunal-confirms-companies-remain-liable-information-provided-ai-chatbot/

**Mata v. Avianca, fabricated cases — confident is not correct** (Activities 4, 5)
https://law.justia.com/cases/federal/district-courts/new-york/nysdce/1%3A2022cv01461/575368/54/

**Samsung data exposure — where the data goes matters** (all activities)
https://techcrunch.com/2023/05/02/samsung-bans-use-of-generative-ai-tools-like-chatgpt-after-april-internal-data-leak/

**Zillow home-flipping shutdown — prediction failure** (Activity 7)
https://investors.zillowgroup.com/news-and-events/news/news-details/2021/Zillow-Group-Reports-Third-Quarter-2021-Financial-Results--Shares-Plan-to-Wind-Down-Zillow-Offers-Operations/default.aspx

Also in the Session 1 set, not reused in Session 2:

- DPD chatbot brand damage — https://www.theguardian.com/technology/2024/jan/20/dpd-ai-chatbot-swears-calls-itself-useless-and-criticises-firm
- CNET AI article corrections — https://www.wired.com/story/cnet-published-ai-generated-stories-then-its-staff-pushed-back/
- iTutorGroup EEOC settlement — https://www.eeoc.gov/newsroom/itutorgroup-pay-365000-settle-eeoc-discriminatory-hiring-suit
- McDonald's AI drive-thru pilot ended — https://apnews.com/article/bebc898363f2d550e1a0cd3c682fa234

---

## Kretz Custom GPTs

- **Kretz AI Decision Guide** (drives Activity 6)
  https://chatgpt.com/g/g-6a427f689a888191b03c01b5608f45ec-kretz-ai-guide
- **Kretz DNA Assistant** (useful in Activity 5 for the outreach tone pass)
  https://chatgpt.com/g/g-6a427b6a557c8191ab8ef594a604fa58-kretz-dna-assistant

**Access rules and fallback.** Signed-in users can interact with GPTs they have
access to; creating or editing a GPT requires a paid plan and is done in the web
experience. If a GPT will not open during the session, paste its short
instructions into a normal chat and continue. Do not spend session time on
logins.

- OpenAI GPTs FAQ — https://help.openai.com/en/articles/8554407-gpts-faq

For the image, file-upload and data-analysis capability claims used to frame the
session, see the corresponding pages in the OpenAI help center. Availability
varies by plan, workspace, and account settings — worth confirming for the
accounts actually in the room rather than assuming.

---

## Prototype tools referenced in Activity 5

The progression these two demonstrate is the point:

1. `Claude_Parcel.html` — the one-shot build. Fast, impressive, missing
   requirements nobody stated.
2. `kretz-landowner-prospecting.html` — the same idea after a conversation
   refined goals, questions, outreach, and workflow.
3. New in Session 2 — the research shots that find the data in the first place,
   which both prototypes assumed you already had.
