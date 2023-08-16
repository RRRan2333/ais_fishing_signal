### Vision
A dashboard that allows people to see the frequencies of AIS signal disappearing. 

The complete product would allow people to view the missing events across the globe, and filter by country, type of fishing vessel. It would also list the top offenders in terms of countries, vessel id, vessel class, vessel size, etc. 

This can be presented as an interactive website or as a Power BI dashboard, with an accompanying article explaining all findings. 

### Ideas
- Plot beginning and ending of missing transponders
- Plot (as lines/arrows) start and end point of missing ships. 
- Time: duration of missing signal; ~~ what time of day did they go missing, etc. ~~
- Mark top X offenders (unique ships)
- Filters by nationality
- Filter by vessle type
- Filter by duration / distance gap
- Overlay missing AIS events with world fishery abbundance data. 
- ~~Get local time of occuring event~~
- How far, on average, does each vessels from each country travel. Do they do this only around neighboring waters or globally? 


### Further
1. Transfer this to Power BI. 
2. Calculate mean or median distance to the country's own shore. Use this to evaluate which countries fish the furthest from their own territories. 
3. Outlier detector: see which countries exhibit the most significant spike at 200 nautical miles. 
3.1 - model after exponential, and figure out decay rate. This method assumes a naive distribution which might not be true. Introduce an interaction term and see the p-value / scale, or some othe way. 
3.2 - clustering: turn histogram into high-dimensional vectors, and cluster (DBSCAN or K-Means) into those that spike at 200, and those that doesnt. 
3.3 - Normalize distribution by country, calculate the normalized frequency of bin  190 to 220 (or 200 to 230), and compare across. 
4. To calculate distance from country's shore, right now it counts all points along a country's border, not just coast / shore. One way to solve it is by subtracting country A's point by all other points, and maybe the resulting points will only be along the shorelines. And repeat this for all countries, then calculate distanceq``

### Source:
1. Original data source: https://globalfishingwatch.org/data-download/datasets/public-welch-et-al-disabling-events:v20221102?itid=lk_inline_enhanced-template


### Helpful links:
1. Sunrise / sunset calculator given coordinates: https://gml.noaa.gov/grad/solcalc/sunrise.html
2. Cool visualization on sunlight duration on earth over the year. 
