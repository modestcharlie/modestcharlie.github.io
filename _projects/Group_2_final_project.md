---
name: Group 2 Final Project
tools: [Python, HTML, Altair]
image: 
description: This is the final project by group 2
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# USGS Earthquakes Data Visualization

We retrieved this data from USGS Earthquakes. [Link Here](https://www.usgs.gov/programs/earthquake-hazards/earthquakes) We used request API to keep updating our data.
```
current_time = datetime.utcnow().strftime('%Y-%m-%dT%H:%M:%S')
api_url = "https://earthquake.usgs.gov/fdsnws/event/1/query"
parameters = {
    'format': 'geojson',  
    'starttime': '2023-01-01',  
    'endtime': current_time,  
    'minmagnitude': 4.5}
response = requests.get(api_url, params=parameters)
data = response.json()
earthquakes = data['features']
```
## Introduction
The dashboard created allows users to explore and understand earthquake events across the globe since January 1, 2023, with a focus on those of magnitude 4.5 or greater. We use a dataset from the U.S. Geological Survey (USGS) public API. 

## Fields and Descriptions
* Longitude (longitude): Geographical longitude of the earthquake occurrence, in degrees (Numerical).
* Latitude (latitude): Geographical latitude of the earthquake location, in degrees (Numerical).
* Depth (depth): Depth at which the earthquake originated beneath the Earth's surface, measured in kilometers. This information is vital for determining the perceived intensity and potential damage caused by the earthquake (Numerical).
* Country or Region (country or region): Derived from the location description, typically indicating the country or nearest region to the earthquake's center (String).
* Magnitude (magnitude): The magnitude of the earthquake, reflecting the energy released during the event, is critical for assessing its potential severity (Numerical).
* Time (time): The timestamp of when the earthquake occurred, provided in UTC and converted to datetime format for easier analysis (Date Time).
* Felt (felt): The number of reports from individuals who experienced the earthquake (Numerical).

## Rows and Columns
* Rows: Each row in the Data Frame equates to an individual earthquake event.
* Columns: Correspond to the aforementioned fields, outlining the characteristics of each earthquake.
This structured dataset serves as a comprehensive resource for analyzing and visualizing earthquake activity globally, making it possible to assess patterns, trends, and potential impacts.


## About the dashboard
The dashboard is divided into several interactive sections. The map section visually displays earthquake locations with red dots on a global map, where users can hover over each dot to see the earthquake's magnitude and the country or region it occurred in. The dashboard also includes plots that let users explore the relationship between the magnitude of earthquakes and other factors such as the number of people who felt the earthquake and the depth at which it occurred. Users can interact with sliders and selections on the dashboard to filter the data based on magnitude or time periods, enabling a tailored analysis. This approach offers an intuitive way for individuals, regardless of their expertise in data science, to engage with and derive insights from the earthquake dataset.

### Contextual Data (Boundary)
See the overlapping part between the following graphs. [Source of Boundary Map](https://www.learner.org/wp-content/interactive/dynamicearth/tectonicsmap/index.html)

<img src="{{site.baseurl}}/assets/pngs/boundary_map.jpg">

{% include final_project.html %}



## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:


<div class="left">
{% include elements/button.html link="https://www.usgs.gov/programs/earthquake-hazards/earthquakes" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/modestcharlie/modestcharlie.github.io/blob/main/_notebooks/Final_Project.ipynb" text="The Notebook" %}
</div>

