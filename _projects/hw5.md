---
name: HW5 – UFO Sightings
tools: [Python, HTML, vega-lite]
image: assets/hw5/hw5_Chart1.png
description: This is a "showcase" project that uses vega-lite for interactive viz! (改项目简介)
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# UFO Sightings in the United States

For this homework I explored a classic UFO sightings dataset and built two interactive vega-lite charts.  (link:"https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv")
The goal is to clean the raw CSV, standardize time and location information, and then help readers quickly see **when** and **where** UFO reports are most commonly appear in recent years.

---


## Visualization 1 – Annual UFO Sightings by State

This line chart shows **how many UFO reports occur each year** for a **single U.S. state**.

- The **x-axis** encodes `year`.
- The **y-axis** shows the count of sightings in that state for that year.
- A dropdown menu lets you choose the state to display, so the chart never gets overcrowded with overlapping lines.
- The chart is built with Altair and exported as a vega-lite JSON spec.

I also created the dropdown to flip between states and compare how reporting trends rise or fall over time.

<vegachart schema-url="{{ site.baseurl }}/assets/hw5/chart1.json" style="width: 100%"></vegachart>


## Visualization 2 – Top 15 States by Total UFO Sightings

The second chart ranks the top 15 states by total UFO reports across the dataset.

- The **x-axis** shows the total number of sightings.
- The **y-axis** lists states, sorted from most to fewest sightings.

Bars shown in this chart are interactive: clicking a bar highlights that state while dimming the others, making it easy to focus on one state while still seeing its context in the ranking.Tooltips show the state name and its total count on hover.

This view answers “Which states report UFOs the most?” in a straightly and helps pick out interesting outliers.

<vegachart schema-url="{{ site.baseurl }}/assets/hw5/chart2.json" style="width: 100%"></vegachart>

## Next Steps (possible)
If there is time, I would like to extend this project in those following aspects:

- Mapping visualizations
  Add an interactive U.S. map showing sightings by state or per-capita normalized counts.

- Time-of-day or seasonality analysis
  Group sightings by hour, month, or season to see when reports are most common.

- Shape-based patterns
  Explore whether certain UFO shapes (“light,” “circle,” “triangle,” etc.) cluster geographically or temporally.



<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Cynthia387/Cynthia387.github.io/blob/main/python_notebooks/hw5.ipynb" text="The Analysis" %}
</div>

