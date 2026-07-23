# Kretz AI Prompting Lab — Session 2 Prompt Pack

Every prompt from the session, in order, in one file. Copy and paste as you go.

Practice runs on the synthetic files in this folder. Real landowner, customer,
pricing, safety, employee, and proprietary information does not go into
unapproved tools.

---

## Activity 1 — Bowl of fruit

```
Create an image of a bowl of fruit.
```

Compare screens with the person next to you. With nothing to go on, the model
returns the statistical middle of everything it has ever seen.

---

## Activity 2 — House in Wisconsin

Generic first:

```
Create an image of a house in Wisconsin.
```

Then structured:

```
Create a realistic image of a house in Wisconsin using: house style, exterior
color, roof, setting, season, time of day, yard details, and purpose. Do not
include address, license plates, mailbox numbers, or identifying personal
details.
```

Then correct it instead of starting over:

```
Keep everything exactly as it is, but change the siding from white to tan,
remove the porch swing, and move the garage to the left side of the house.
```

**The reusable template.** Fill every slot:

```
[What it is] — [style and era], [materials and colors], [distinguishing
features], [surroundings], [location], [season and time], [light],
[vantage point], [format].
```

---

## Activity 3 — Intention changes output

Same image, two different reasons:

```
Transform the same house into a black-and-white coloring page for a child.
```

```
Transform the same house into an architectural concept image for a remodel
conversation.
```

**The reusable template.** The single highest-leverage habit in the session:

```
[Do this thing] for [who is going to read it], because [what happens next].
Keep it [length and format]. [What to leave out].
```

It works on text too. Compare "summarize this meeting" against "summarize this
meeting into five bullets the yard crew can read at the start of shift."

---

## Activity 4 — Spreadsheets by prompt

**Behavior rule: AI is not a calculator.** Use it to propose structure and formulas; make it show its work, let Excel perform the arithmetic, and verify the result.

File: `spreadsheet_builder_haul_costs_synthetic.csv`

Step 1, structure:

```
Create a spreadsheet plan for tracking haul costs. Include columns, sample
rows, formulas, cost per mile, cost per MBF, assumptions, and review warnings.
```

Step 2, the one that matters most:

```
Now give me the actual Excel formulas in the cells — do not give me the
calculated numbers. Flag anything you had to assume.
```

Step 3, the collapse:

```
Looking back at everything we just built together, how could I have gotten all
of this from a single prompt? Write me that prompt, then explain which parts of
it were doing the work.
```

**Watch for:** four problems are planted in that CSV. A zero board-feet row, a
blank fuel reading, an impossible 26.5 driving hours, and 3 miles to Stevens
Point. If the model hands back tidy numbers without mentioning any of them,
that is the lesson.

---

## Activity 5 — Landowner research boundaries

The research shots first. These ask where public records live — no Kretz data
goes anywhere.

```
How can I find all the landowners in a single Wisconsin county using free,
public data? I want owner names, mailing addresses, and acreage. Tell me
exactly where that data lives, who publishes it, what format it comes in, what
it costs, and how current it is.
```

```
Now narrow it down. I only want private forested parcels big enough to be worth
a conversation about timber. In Wisconsin parcel data, which field tells me a
parcel is forest land, and what are the actual class codes? What acreage
threshold makes sense, and why? Also explain how Managed Forest Law enrollment
works and what its minimum acreage requirements are.
```

```
Where do I get Managed Forest Law spatial data for Wisconsin, and how would I
join it to the county parcel data? Give me the portal, the layer name, and the
field I would join on. Tell me plainly what parts of MFL are published publicly
and what parts are not.
```

Then the activity, on the synthetic file
`landowner_public_research_synthetic.csv`:

```
Using the synthetic landowner research CSV, create a verification checklist and
a careful outreach draft. Do not estimate timber value, imply Kretz inspected
the property, or treat public data as verified.
```

**Watch for:** that file has a blank mailing city, a 0.4-acre parcel classed as
forest, an out-of-state address that does not match its city, four owners on
more than one parcel, and four MFL records with no expiration year. It has no
email column, because real parcel data does not have one.

---

## Activity 6 — Operational efficiency

File: `operational_efficiency_prompts_synthetic.csv`. Best run inside the Kretz
AI Decision Guide.

```
Using the operational efficiency CSV, classify each task as existing software
first, narrow Custom GPT, automation, process cleanup, vendor system, or do not
use AI yet.
```

Then add what actually constrains you:

```
Now redo the top three with my actual constraints: who is on shift, what
equipment is down, and what has a hard deadline this week. If a constraint makes
your recommendation wrong, say so instead of working around it.
```

**Watch for:** if every task comes back as "use AI," the prompt was too loose.
Several of these are Outlook problems, not AI problems.

---

## Activity 7 — Price movement scenarios

**Behavior rule: AI cannot forecast lumber prices.** Use it to organize supplied evidence and build monitoring scenarios, never to invent the next price.

File: `lumber_price_movement_practice_synthetic.csv`. These are invented index
numbers, not lumber prices.

```
Using the synthetic lumber price movement data, identify patterns and possible
leading indicators. Do not make a prediction as fact. Give scenarios,
assumptions, confidence, and source-verification needs.
```

The deliverable worth keeping:

```
Now turn that into a one-page monitoring template: the drivers worth tracking,
where each number comes from, how often to check it, and what a meaningful
change looks like versus normal noise. Use only what is in the data I gave you.
If something is not in it, say so rather than filling it in.
```

**Watch for:** price follows housing starts at a three-month lag — that fits
measurably better than no lag. All four species follow the same driver; what
differs is how far each one moves. Diesel, export demand and log supply are
mathematically unrelated to price by construction. If the model explains why
diesel drives maple prices, it invented a story about numbers that contain none.

---

## Activity 8 — Build a tiny HTML tool

```
Build a single-file HTML tool to help with this problem: [describe problem]. It
should have inputs, output, review warning, no external dependencies, and a
print button. Ask up to five questions before coding if needed.
```

Then refine — two changes, not twenty:

```
Two changes only. [First change.] [Second change.] Leave everything else
exactly as it is.
```

**The five things a tool request needs:** what it does, who uses it, what goes
in, what comes out, and the constraints.

Follow-along example: the timber sale tracker in
`kretz_prompt_to_tool_builder_example.html`, with both prompts that built it
printed on the page.

---

## Voice work — any activity

File: `kretz_voice_samples_session2_synthetic.txt`. Best run inside the Kretz
DNA Assistant.

```
Read these voice samples. Describe the Kretz voice in six rules, then rewrite
the draft at the bottom of the file to match it.
```

---

## The four templates worth keeping

**Specificity.**

```
[What it is] — [style and era], [materials and colors], [distinguishing
features], [surroundings], [location], [season and time], [light],
[vantage point], [format].
```

**Intention.**

```
[Do this thing] for [who is going to read it], because [what happens next].
Keep it [length and format]. [What to leave out].
```

**Data.**

```
Build [what] with columns for [fields]. Add [calculation] and subtotals by
[grouping]. Write the actual formulas in the cells — not the computed numbers.
Flag anything you had to assume.
```

**Teach me back.** Use after anything that took more than three tries.

```
Looking back at everything we just worked through, how could I have gotten this
from a single prompt? Write me that prompt, then tell me which parts of it
mattered most.
```
