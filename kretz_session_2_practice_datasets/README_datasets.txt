KRETZ SESSION 2 — PRACTICE DATASETS
===================================
All files are SYNTHETIC. No real landowner, customer, employee, pricing, or
market data appears anywhere in this folder. Generated for the Session 2
prompting lab so participants can practice on realistic data without any of
it being real.

Upload one file at a time into ChatGPT or a Custom GPT and run the matching
prompt from the handout.


-------------------------------------------------------------------
spreadsheet_builder_haul_costs_synthetic.csv                             ACTIVITY 4
-------------------------------------------------------------------
28 loads out of the Antigo yard. Raw inputs only — no calculated columns,
on purpose. The point of the activity is that the AI writes the formulas
and Excel does the arithmetic.

Columns: load_id, date, origin, destination, one_way_miles, species, grade,
board_feet, truck_id, driving_hours, fuel_gallons, fuel_price_per_gal,
driver_rate_per_hour, tolls_and_permits

To get cost per mile and cost per MBF the model has to derive fuel cost,
driver cost, a round-trip assumption, and divide board feet by 1,000. None
of that is in the file. That is the exercise.

FOUR PROBLEMS ARE PLANTED IN THIS FILE:
  HL-1007  board_feet = 0          -> divide by zero on cost per MBF
  HL-1014  fuel_gallons blank      -> silently drops fuel cost if unguarded
  HL-1020  3 miles to Stevens Point-> destination/mileage mismatch
  HL-1023  driving_hours = 26.5     -> impossible in one day

A model that returns tidy numbers without mentioning any of these has just
demonstrated the lesson. Ask the room which rows it should have caught.

Answer key: kretz_haul_costs_reference_workbook.xlsx (in the repo root)


-------------------------------------------------------------------
landowner_public_research_synthetic.csv                     ACTIVITY 5
-------------------------------------------------------------------
36 fictional parcel records shaped like real Wisconsin parcel data, so the
column names match what participants would actually download.

Columns: record_id, owner_name, mailing_city, mailing_state, parcel_id,
town, acres, property_class, mfl_status, mfl_expiration_year, last_contact,
source_notes

Property classes follow Wisconsin s. 70.32(2)(a): 6 = productive forest,
5M = agricultural forest, 5 = undeveloped, 1 = residential.

PROBLEMS PLANTED:
  - one record with a blank mailing city
  - one 0.4-acre parcel classed as forest (far under the MFL minimum)
  - one out-of-state mailing address that does not match its city
  - four owners who appear on more than one parcel, so a naive count
    double-counts both the owners and the acreage
  - four MFL/FCL records with no expiration year recorded

Note there are NO email addresses in this file, because real parcel data
does not contain them. That is deliberate and worth pointing out.


-------------------------------------------------------------------
operational_efficiency_prompts_synthetic.csv                 ACTIVITY 6
-------------------------------------------------------------------
22 real-shaped tasks across Sales, Forestry, Mill Operations, Logistics,
Office/Admin, HR, and Maintenance.

Columns: task_id, department, task_description, frequency,
minutes_per_occurrence, people_involved, current_tool, pain_point,
data_sensitivity

Deliberately mixed so the Decision Guide has to sort them. Several are
plainly "existing software first" (scheduling across four calendars is
Outlook, not AI). Several are process problems that AI would only paper
over. A few are genuinely good AI candidates. One — summarizing exit
interview themes — is marked employee-sensitive and should trigger a
conversation about what belongs in an approved tool at all.

If every task comes back as "use AI," the classification prompt was too
loose. That is a useful failure to run into live.


-------------------------------------------------------------------
lumber_price_movement_practice_synthetic.csv                  ACTIVITY 7
-------------------------------------------------------------------
36 months x 4 species of INVENTED index data. These are not lumber prices.
They are numbers generated to have a findable pattern.

Columns: month, species, grade, price_index, housing_starts_index,
mortgage_rate_pct, export_demand_index, log_supply_index,
diesel_price_index, notes

A deliberate relationship was planted in this synthetic dataset, and it is verifiable:

  - price_index follows housing_starts_index with a THREE-MONTH LAG.
    Correlation at lag 3 is 0.84 to 0.88 across all four species, versus
    0.67 to 0.77 with no lag. The lag genuinely fits better.
  - All four species follow the same driver. What differs is HOW FAR they
    move: hard maple swings about 63 index points across the period, red
    oak 52, white ash 33, basswood 18. Sensitivity, not direction.
  - export_demand_index, diesel_price_index and log_supply_index are
    deliberate red herrings. Their correlations with price round to 0.00
    at two decimal places.

So if the model reports that diesel or export demand drives maple prices,
it has invented a story about numbers that provably contain none. And if
it reports a housing-starts relationship without noticing the lag, it has
found the weaker version of the planted answer.

That is the whole activity. Use it.


-------------------------------------------------------------------
kretz_voice_samples_session2_synthetic.txt                    DNA / ACTIVITY 5
-------------------------------------------------------------------
Four paired examples: a generic AI version and a Kretz version of the same
message, plus six rules describing the voice and one bad draft to rewrite.

Use with the Kretz DNA Assistant, or paste into a normal chat with:
"Read these samples. Describe the voice in six rules, then rewrite the
draft at the bottom to match it."


-------------------------------------------------------------------
BEFORE YOU UPLOAD ANYTHING ELSE
-------------------------------------------------------------------
These files exist so nobody has to reach for a real one. Practice stays on
synthetic data. Real landowner, customer, pricing, safety, employee, and
proprietary information does not go into unapproved tools, and that rule
does not pause for training.

One more boundary for the landowner activity. Public availability does not
by itself make every use appropriate. Records being public means you may
look at them; it does not mean any outreach is automatically fine. Decide
on acceptable outreach practices, review every message before it goes out,
avoid protected or suppressed records, and give anyone you contact a
respectful way to decline future contact.
