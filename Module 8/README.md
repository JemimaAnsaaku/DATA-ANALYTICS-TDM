# Introducing Tableau


<details><summary> What even is Tableau? </summary>

It’s a tool. A program I can use on my computer. Purpose = take data (spreadsheets, databases, etc.) - i can turn into pictures (charts, dashboards, visuals) - so I can see patterns fast. Basically: instead of staring at numbers, I see shapes.

Why not just use Excel?

Excel is fine for small stuff.

But when the data is huge, or I need dashboards that update, or I want to share with people who don’t like spreadsheets → Tableau is better.

It’s built for visual analysis first, not just calculating.

## How does Tableau actually connect to my data?

I give it a file (Excel, CSV) or a live connection (like SQL database).

Tableau doesn’t store the data (unless I import as an extract) → it’s more like a window into my data.

### What’s the deal with “dimensions” vs “measures”?

Dimension = categories, labels, stuff I group by (like Country, Date, Product).

Measure = numbers I can add up, average, count (like Sales, Profit, Quantity).

Easy test: If I ask “How much/many?” - that’s a measure. If I ask “By what group?” → that’s a dimension.

### Why do people talk about rows and columns in Tableau?

Because Tableau builds visuals by dragging fields into either rows or columns.

Rows = what goes across horizontally. Columns = what goes vertically.

Example: Sales (number) on rows, Region (category) on columns → boom, bar chart.

### What’s a dashboard?

One screen that shows multiple visuals together (charts, maps, filters).

Why? So the viewer doesn’t have to click around. They can see a story in one shot.

But how do I actually “analyse” with it?

I drag fields around, change chart type, filter stuff, highlight patterns.

The whole point is “visual thinking” → let the picture show me trends I wouldn’t notice in a raw table.

### What’s Tableau not good for?

Heavy duty data cleaning (that’s better in SQL, Python, or Excel before Tableau).

Super complex stats (Tableau can do some math but not everything).

It’s more about speed of insight than about being a calculation engine.

### Why should I care?

If I can turn raw messy numbers into clear visuals → I can explain things better, faster.
People trust what they can see.
</details>

<details><summary> Visualising data with Tableau </summary>

## Tableau visualisations — step-by-step 

### Step 1 — Connect to data

I open Tableau and connect to a file or database, choosing Live (fresh, can be slower) or Extract (faster snapshot).

Why: This choice affects speed, refresh strategy, and what my audience sees.

### Step 2 — Inspect fields (Data Pane)

I check data types (number, string, date) and whether fields land as Dimensions (categorical) or Measures (numeric).

I fix names, set default aggregations (SUM vs AVG), and create calculated fields if needed.

Why: Bad types or wrong default aggs = wrong charts and misleading results.

### Step 3 — Decide the question and the grain

I state what one mark should represent (e.g., one mark per country per month).

Why: Grain controls the number of marks and prevents double counting.

### Step 4 — Build the view skeleton (Rows/Columns)

I drag Dimensions (e.g., Category to Columns, Region to Rows) to set headers.

I drag a Measure (e.g., Sales) to create an axis.

Why: Layout shelves define the structure before I worry about looks.

### Step 5 — Pick discrete vs continuous on purpose

Blue pills (discrete) make headers and buckets; green pills (continuous) make axes and ranges.

Why: The same field behaves very differently; this is the difference between a bar chart by month name (discrete) and a time series (continuous).

### Step 6 — Choose the chart type

I use Show Me for quick suggestions or switch the Marks type (bar, line, map, scatter).

Why: Chart choice should match the task (compare parts, trends, relationships, distribution).

### Step 7 — Encode with the Marks card

I place fields on Color, Size, Label, Detail, Tooltip, and sometimes Shape.

I keep one main message per chart and avoid over-encoding.

Why: Good channels amplify the message; too many encodings create noise.

### Step 8 — Filter the data

I drag fields to Filters (discrete pick lists, continuous ranges, relative dates) and show filters to users if needed.

I use context filters when other filters depend on them.

Why: Filters change the dataset before visualising; they affect totals, performance, and truth.

### Step 9 — Sort and focus

I sort by a measure, create Top N filters, or highlight key categories.

Why: Ordered views surface signal faster than alphabet soup.

### Step 10 — Drill down with hierarchies

I create hierarchies (Year → Quarter → Month → Day or Country → State → City) for click-to-drill.

Why: Lets me start broad and reveal detail without building 5 separate charts.

### Step 11 — Add quick table calculations

I use percent of total, running sum, moving average, rank; then check addressing/partitioning.

Why: Table calcs answer “compared to what?” but only if they’re computed across the right dimension.

### Step 12 — Combine measures (dual/combo axes)

I put two measures on a dual axis and synchronise if they share units; or use a combo of bars and lines.

Why: Helps compare related trends; unsynchronised scales can mislead.

### Step 13 — Use the Analytics pane

I drop in reference lines/bands, trend lines, forecasts, box plots.

Why: These add context (targets, averages, uncertainty) beyond raw bars and lines.

### Step 14 — Polish formatting

I set number formats, axis ranges, labels, and readable tooltips; I reduce non-data ink.

Why: Clean formatting lifts comprehension and prevents misreads (e.g., currency without symbols).

### Step 15 — Add interactivity with parameters

I build parameters for user-chosen measures, thresholds, or scenario inputs, paired with calc fields.

Why: Parameters let users ask “what if?” without me rebuilding the viz.

### Step 16 — Assemble dashboards

I bring sheets into a dashboard, use containers for layout, and add actions (filter, highlight, URL).

I test on Device Designer for phone/tablet.

Why: Insights live across multiple views; actions turn passive charts into exploratory tools.

### Step 17 — Validate the logic

I compare totals to a known source, check mark counts vs expected grain, and sanity-check outliers.

Why: A pretty wrong chart is still wrong; validation catches silent errors.

### Step 18 — Mind performance

I prefer extracts when sources are slow, hide unused fields, limit marks, and use context filters wisely.

Why: Fast dashboards get used; slow ones get closed.

### Step 19 — Publish and share

I publish to Tableau Public, add captions/instructions, and ensure filters/parameters are obvious.

Why: Clear sharing reduces support questions and misinterpretations.

### Step 20 — Common pitfalls I watch for

Wrong grain (too many dimensions) inflates totals.

Default SUM where AVG or COUNTD is correct.

Discrete dates when I meant a continuous time axis.

Dual axes not synchronised.

Color scales without meaningful order or midpoint.

Filters applied to one sheet but not the dashboard.

Why: These are the traps that make good data look bad or say the wrong thing.

</details> 

<details><summary> Tableau dashboards </summary>

## Introduction to Dashboards

A Tableau dashboard is basically a single screen where I can bring together several different charts and visualisations.
Rather than flicking between separate tabs, I can see everything side by side, which makes it much easier to compare and make sense of the data.
To me, the main point of a dashboard is convenience and clarity.

### Static and Live Data

Static data means the dashboard shows a fixed snapshot of the numbers at one point in time. That’s fine if I’m reporting last year’s results, but it goes stale quickly.

Live data updates automatically, so the figures on the dashboard always stay current. That’s important if I’m tracking something that changes constantly, like sales, stock levels, or trending hashtags.

My understanding is that static is for reporting the past, live is for monitoring the present.

### Dashboard Benefits

Dashboards let me pull in data from multiple sources and display it all on one screen.

They’re interactive, so I can filter things down, zoom into maps, or drill into specific details.

They’re both a summary and an exploration tool, depending on how I use them.

For me, the biggest win is saving time and helping people make decisions faster.

### Dashboard Best Practices

I need to know who’s looking at the dashboard and what they actually need from it.

Keep the data clean and relevant — clutter just confuses.

Choose the right chart type for the story I’m telling.

Use templates if possible, to keep things tidy and consistent.

Don’t overdo it with colours, annotations, or too many visuals at once.

Get feedback and be prepared to refine the design based on what users say.

### Creating a New Dashboard

In Tableau, I click the “New Dashboard” button at the bottom to create one.

I then drag my charts (sheets) into the dashboard space and arrange them.

There’s technically no limit to how many I can add, but cramming loads in makes it messy.

Each chart is linked back to its worksheet, so if I update the worksheet, the dashboard updates automatically too. Handy, but it means I need to watch my edits.

### My Overall Takeaways

A Tableau dashboard is just a collection of visualisations on one page.

Static data = frozen in time, live data = keeps updating.

The tricky bit is design: keeping it simple, clear, and genuinely useful for the audience.

</details>
