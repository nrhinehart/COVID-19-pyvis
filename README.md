# COVID-19-pyvis
Pulls the latest COVID-19 data and provides a few Python functions to plot time-series data for different kinds of regions: Countries, States, and Counties.

It automatically interfaces with a <a href="https://github.com/CSSEGISandData/COVID-19">repo of daily time-series data</a> maintained by the JHU CSSE</a>
# Installation

This module depends on a submodule. Thus, the easiest thing to do is clone it like so:

`git clone --recursive https://github.com:nrhine1/covid-19-pyvis` <br>

Then, install the requirements

`pip3 install -r requirements.txt`

Tested with Python 3.7.0 on MacOS. I recommend you use a virtualenv or create a conda env.

e.g. 
```virtualenv -p `which python3` covidpy; 
source covidpy/bin/activate; 
pip install -r requirements.txt```

# Usage
See the [jupyter notebook](covid-19-analysis/notebooks/overview_plotting_example.ipynb) for a walkthrough.

The core functionality is currently provided by several functions defined therein:

- `plot_regions([list of country or region names])`
- `plot_states([list of US state two-letter codes])`
- `plot_counties([list of US county names])`.

# Examples:
## Plot worldwide summary.
`plot_regions(region_names=regions)`<br>
<img src="examples/global_2020-03-09.png" width=400>

## Plot data for a few specific countries:
`plot_regions(['Mainland China'])`<br>
<img src="examples/mainland_china_2020-03-09.png" width=400>

`plot_regions(['South Korea'])`<br>
<img src="examples/south_korea_2020-03-09.png" width=400>

`plot_regions(['US'])`<br>
<img src="examples/usa_2020-03-09.png" width=400>

## Aggregate across several countries:
`plot_regions(['France', 'Italy', 'Germany', 'Spain'])`<br>
<img src="examples/france_italy_germany_spain_2020-03-09.png" width=400>

## Sometimes the data stores special cases as "Regions", like the Diamond Princess Cruise Ship:
`plot_regions(["Diamond Princess cruise ship"])`<br>
<img src="examples/diamond_cruise_ship_2020-03-09.png" width=400>

## Plot data for a specific state in the United States:
`plot_states(['WA'])`<br>
<img src="examples/washington_state_2020-03-09.png" width=400>

## Aggregate across a few states
`plot_states(['NY', 'PA'])`<br>
<img src="examples/ny_state_pa_state_2020-03-09.png" width=400>

`plot_states(['CA', 'WA'])`<br>
<img src="examples/ca_state_wa_state_2020-03-09.png" width=400>

