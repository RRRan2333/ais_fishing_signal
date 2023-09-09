### Introduction
This repo hosts everything that supports the article "[*Silent Signals, Open Seas*](https://geran.notion.site/Silent-Signals-Open-Seas-74ad7a55236e48a1afbdd17e119f427e)", except the main body of the article. The original datasets that support the analyses presented in the article, the Python code that handles data manipulations, calculations, and visualizations, and the Power BI notebooks that are embedded into the article to allow user interaction are all hosted here.

### Vision
An educational article with dashboards that allow users to interact and explore the patterns of Illegal, Unreported, and Unregulated (IUU) fishing behaviors of countries. 

### Potential features to be included in future iterations
- Plot the beginning and ending of missing AIS signals
- Plot (as lines/arrows) start and end points of missing vessels
- Overlay missing AIS heatmap on world fishery abundance data. 
- Improve the 'distance from homeland' calculation by using only coastlines, rather than the entire border. This can be achieved by subtracting the border nodes/points that overlap with other countries.

### Source:
1. Original data source: https://globalfishingwatch.org/data-download/datasets/public-welch-et-al-disabling-events:v20221102?itid=lk_inline_enhanced-template
2. Academic paper: Welch et al. (2022) - Hotspots of unseen fishing vessels: https://www.science.org/doi/10.1126/sciadv.abq2109
