# Real-Estate Analysis of Vancouver Neighbourhoods

## Introduction

In terms of realty analytics, it often involves understanding the basic concepts surrounding the ability of a property's value and obtainable revenue. This, in turn, provides the reason for investment and lots of planning and decision-making for it to succeed. A neighbourhood/community-wise Analysis of Residential Real Estate would provide a better understanding in determining which neighbourhood would offer a good return on investment, which is the goal of this project.

Vancouver is one of the largest and most populous cities in Canada, known for being diverse, multicultural and home to world class-amenities, making it a great place to invest in a house(or an apartment)!

When investing in a property, an overall market analysis will provide a good idea of the trends, but more is needed. It is imperative to buy property in the right neighbourhood because even if the overall market is excellent, a wrong location may lead to decreased property value in the future.

A Neighbourhood Analysis will reveal the investment potential of various neighbourhoods based on their characteristics and intrinsic values.

### Target Audience

This analysis aims to provide more detailed insight for both companies(real estate firms) & individuals who are interested in investing in residential property in Vancouver. In addition, this analysis will provide a comprehensive understanding of the most suitable neighbourhood according to one's needs.


### Part 1: Crime statistics

In terms of value and investment return, a desirable real estate property would exhibit certain features related to pricing, ease of transportation, distance to amenities, and a relatively low crime rate in the neighbourhood. In this section, I’ll demonstrate how Data Science can use pattern detection to identify appealing locations for investment in the metro Vancouver area. The data used in this section was gathered from Vancouver Open Data Catalogue. The data ranges from the year 2003 up to 2017. In addition, I have added serval modifications to the data to illustrate location information better. 

let us start with importing the necessary packages
```
import pandas as pd  
import numpy as np
import matplotlib as mpl
import matplotlib.pyplot as plt
import math
import geopandas
import geopy
from geopy.geocoders import Nominatim
import folium
from geopy.extra.rate_limiter import RateLimiter
from folium import plugins
from folium.plugins import MarkerCluster
from pyproj import Proj
```

The by looking at the raw data we can see that it contains serval feature sets regarding a single incident. 
```
df = pd.read_csv('crime_records.csv')
df.head(5)
```
![Image](Capture0.PNG)
