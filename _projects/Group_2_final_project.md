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
{% include final_project.html %}





## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:


<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

