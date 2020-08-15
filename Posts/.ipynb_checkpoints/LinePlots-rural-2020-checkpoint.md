# Pollution in Indian Cities: A more Diverse Set

In the previuos post [here](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts./LinePlots-urban-2020.md), we took a look a pollution levels in Major cities like Mumbai, Delhi, Bengaluru, Chennai, Kolkata and Visakhapatnam and the impact of lockdown. In this post, we focus on a more diverse set of cities across India namely `Mussoorie`, `Vapi`, `Kota`, `Jabalpur`, `Coimbatore`, `Guwahati`. to see their trends in pollution levels as lockdown due to COVID is gradually lifted.

The major components of air pollution are `particulate matter of sizes 2.5 microns and 10 microns` in width (PM2.5 and PM10 respectively), and gases such as `Carbon Monoxide` (CO), `Nitrogen Dioxide` (NO<sub>2</sub>), `Sulpher Dioxide` (SO<sub>2</sub>) `Ozone` (O<sub>3</sub>). In this post we focus on the PM2.5 levels.For details about pollutants and their consequences refer this [post](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts/Pollutants%20Description.md).

# Generating the Visualization
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

## The Overall trend

<img src="../code/images/rural_pm2.5_bar.png"   /><br>
Fig 1 : PM2.5 values for 6 Indian cities represented as a Bar Chart<br>

This figure shows `stacked bar chart` of daily median values for `PM2.5` across various cities. This gives a high-level overview of the trends across the cities in a single chart. X axis is Dates and Y axis represents median values of pollutants calculated over a 24-hour frame. 
 
## Lets plot some!

<img src="../code/images/rural_pm2.5_3city_line.png"  /><br>
Fig 2 : PM2.5 values for Vapi, Kota, Mussoorie, Combatore as line chart. Here the `Green` Line represents `NAAQS` standards and `Yellow` Line represents `WHO` standards.

Few details are very evident from `Fig 1` and `Fig 2`. Cities like Vapi,which also houses GIDC (Gujurat Industrial Development Corporation) and Guwahati with somewhat higher PM2.5 levels show decrease as we approach May. Reduction in Vapi is most likely due to this Industrial area coming to standstill due to Lockdown. As we move towards June most of the cities have their PM2.5 levels under NAAQS standards but still above WHO guidelines with Mussoorie, a hill station, being the exception, whose levels were under WHO's recommended levels most of the June. This is a bit to cluttered lets focus on a couple of cities!

## A tale of 2 Cities
<img src="../code/images/rural_pm2.5_2city_line.png"  /><br>
Fig 3: PM2.5 values for Mussoorie and Coimbatore.

Lets consider `Mussoorie`, a hill station in the north and `Coimbatore`, a city in the South. One would assume Mussoorie to be far less polluted compared to a Coimbatore. However the margins are quite colse between them! Mussoorie shows a reduction in PM2.5 levels as we enter April and sudden rise in May, reducing again in June. It is to be moted that Mussoorie is the only city to falls below under WHO levels from all the cites considered. Coimbatore shows a minuscule reduction during Lockdown and large swing towards the end of July, mostly like being data collection errors.

## Hill Station Vs Industrial Area

<img src="../code/images/rural_pm2.5_hl-indst_line.png"/><br>
Fig 4: PM2.5 - Mussoorie and Vapi

When comparing Vapi, where GIDC (Gujurat Industrial Development Corporation) is located against Mussoorie, a hill station, the positive effects of lockdown are clearly visible. Vapi, an industrial area came to halt during lockdown the and the pollution levels show clear decline, and after June the levels are same as a hill station!

### PM2.5 for all cities
<img src="../code/images/rural_pm2.5_all_cities.png"  width=100% /><br>
Fig 5: PM2.5 values for all the cities.

Vapi and Guwahati, the most polluted of the bunch, followed by Jabalpur show a notable decline in PM2.5 levels. Kota and Coimbatore show little reduction, mostly because PM2.5 levels we already low to begin with.


### Plot them all!
<img src="../code/images/rural_all_allcities.png"   width=100% /><br>
Fig 6: All the polltants for every city.


As we move from January to July Vapi and Guwahati show significant reduction in their `PM2.5` and `PM10` maybe because these we more polluted in the first place. On the contrary Mussoorie and Coimbatore show little to no reduction furthermore Coimbatore even show a bit of increase in PM2.5 and PM10 levels towards July. `CO` levels show steep reduction for Vapi and Guwahati after the lockdown and `O3` shows a decline for Coimbatore whereas an increase for Guwahati. We also have some missing data i.e `CO` for Mussoorie. This provides a concise and visually interesting way to look and pollution trends within our Country’s cities.

### Another angle for you to ponder about!
<img src="../code/images/rural_all_allcity_trans.png"  width=100% /><br>

### Github

Find the link to our code for these visualizations [here](https://github.com/algoasylum/ExploringTheUnseen/blob/master/code/Simpe%20line%20plots.ipynb) 
