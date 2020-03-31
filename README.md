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

# Note: the naming conventions of the raw data have changed over time. Thus, until they have been stable for awhile, I wouldn't recommend treating the results plotted herein as authoritative!

# Usage
See the [jupyter notebook](covid-19-analysis/notebooks/overview_plotting_example.ipynb) for a walkthrough.