# Vision
A dashboard that allows people to see the frequencies of AIS signal disappearing. 

The complete product would allow people to view the missing events across the globe, and filter by country, type of fishing vessel. It would also list the top offenders in terms of countries, vessel id, vessel class, vessel size, etc. 

This can be presented as an interactive website or as a Power BI dashboard, with an accompanying article explaining all findings. 

# MVP
- ~~Time: duration of missing signal; ~~
- ~~what time of day did they go missing, etc. ~~
- ~~Mark top X offenders (unique ships)~~
- ~~Filters by nationality~~
- ~~Filter by vessle type~~
- ~~Filter by duration / distance gap~~
- ~~Get local time of occuring event~~
- ~~How far, on average, does each vessels from each country travel. Do they do this only around neighboring waters or globally? ~~


### MVP+
1. ~~Transfer this to Power BI. ~~
2. ~~Calculate mean or median distance to the country's own shore. Use this to evaluate which countries fish the furthest from their own territories. ~~: ~~To calculate distance from country's shore, right now it counts all points along a country's border, not just coast / shore. One way to solve it is by subtracting country A's point by all other points, and maybe the resulting points will only be along the shorelines. And repeat this for all countries, then calculate distanceq``~~
3. ~~Share of missing period in daytime vs late night. ~~
4. ~~Include continents, and add group countries (color code) by corresponding continents, not country specific. ~~
5. ~~Added 'noise' col to hopefully present information better for the two 1-D bubble plots, mimicing a beeswarm plot, although i'm not sure if it is working well. ~~

- Plot beginning and ending of missing transponders
- Plot (as lines/arrows) start and end point of missing ships. 
- Overlay missing AIS events with world fishery abbundance data. 
- Better 'distance from homeland' calc by only using coastlines, rather than entire border. This can be achieved by subtracting the boarder nodes / points that overlaps w other countries. 


# Ver 2:

### Country profile page
##### On dashboard: 
1. Distribution of tonnage
2. Share of kinds of vessel
3. Elbow graph (distance to shore when gap starts; histogram)
4. Compared to overall all country elbow graph

##### Outside of dashboard:
1. Ranking, illicit fishing. 
2. Distance traveled? Start and finish, pin point? Somehow visualize the travel? 

### Outlier detector: see which countries exhibit the most significant spike at 200 nautical miles. 
##### Methods: 
1. model after exponential, and figure out decay rate. This method assumes a naive distribution which might not be true. Introduce an interaction term and see the p-value / scale, or some othe way. 
2. clustering: turn histogram into high-dimensional vectors, and cluster (DBSCAN or K-Means) into those that spike at 200, and those that doesnt. 
3. Normalize distribution by country, calculate the normalized frequency of bin  190 to 220 (or 200 to 230), and compare across. 
##### Presentation: 
A separate page / report on Power BI that doesn't allow multiple selections. Only one country can be highlighted, so that it can go more in depth: including distribution of gap time, gap distance, and dist from shore before disabling. 


### Source:
1. Original data source: https://globalfishingwatch.org/data-download/datasets/public-welch-et-al-disabling-events:v20221102?itid=lk_inline_enhanced-template
2. WaPo Article: https://www.washingtonpost.com/climate-environment/interactive/2023/map-illegal-fishing/

### Helpful links:
1. Sunrise / sunset calculator given coordinates: https://gml.noaa.gov/grad/solcalc/sunrise.html

