# Pollution in Indian Cities: The Rural Angle

In the previuos post [here](wer), we took a look a pollution levels in Major cities like Mumbai, Delhi, Bengaluru, Chennai, Kolkata and Visakhapatnam and the impact of lockdown. In this post, we focus on some of the lesser developed cities namely `Mussoorie`, `Vapi`, `Kota`, `Jabalpur`, `Coimbatore`, `Guwahati` to see their trends in pollution levels as lockdown due to COVID is gradually lifted.

The major components of air pollution are `particulate matter of sizes 2.5 microns and 10 microns` in width (PM2.5 and PM10 respectively), and gases such as `Carbon Monoxide` (CO), `Nitrogen Dioxide` (NO<sub>2</sub>), `Sulpher Dioxide` (SO<sub>2</sub>) `Ozone` (O<sub>3</sub>). In this post we focus on the PM2.5 levels.

# Generating the Visualization
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

<img src="../code/images/rural_pm2.5_bar.png"   /><br>
Fig 1 : PM2.5 values for 6 Indian cities represented as a Bar Chart<br>

In this article we plot line and bar charts of various pollutants for 6 cities, across India. Here dates are plotted on X axis and `Y axis` represents the `median values of pollutants` observed over a 24-hour frame.<br>

# Observations 
### Lets plot some!

<img src="../code/images/rural_pm2.5_3city_line.png"  /><br>
Fig 2 : PM2.5 values for Vapi, Kota, Mussoorie, Combatore as line chart. Here the `Green` Line represents `NAACQ` standards and `Yellow` Line represents `WHO` standards.

Few details are very evident from `Fig 1` and `Fig 2`.Cities like Vapi and Guwahati with somewhat higher PM2.5 levels show decrease as we approach May. In Fig2, Green and black lines represent WHO and NAACQ recommended levels. As we move towards June most of the cities have their PM2.5 levels under NAACQ guidelines but still above WHO guidelines with Mussoorie being the exception, whose levels were under WHO's recommended levels most of the June. This is a bit to cluttere lets focus on a couple of cities!

## A tale of 2 Cities
<img src="../code/images/rural_pm2.5_2city_line.png"  /><br>
Fig 3: PM2.5 values for Mussoorie and Coimbatore.

Lets consider `Mussoorie`, a hill station in the north and `Coimbatore`, a city in the South. Mussoorie shows a reduction in PM2.5 levels as we enter April and shows increase in May, reducing again in June. Also Mussoorie is the only city to falls below under WHO levels from as the cites considered. Coimbatore show a slight reduction di=uring lockdown period but levels of PM2.5 starts to rise from June to July.

### PM2.5 for all cities
<img src="../code/images/rural_pm2.5_all_cities.png"  width=100% /><br>
Fig 4: PM2.5 values for all the cities.

### Plot them all!
<img src="../code/images/rural_all_allcity.png"   width=100% /><br>
Fig 5: All the polltants for every city.

# Conclusion
As we move from January to July Vapi and Guwahati show significant reduction in their `PM2.5` and `PM10` maybe because these we more polluted in the first place. On the contrary Mussoorie and Coimbatore show little to no reduction furthermore Coimbatore even show a bit of increase in PM2.5 and PM10 levels towards July. `CO` levels show steep reduction for Vapi and Guwahati after the lockdown and `O3` shows a decline for Coimbatore whereas an increase for Guwahati. We also have some missing data i.e `CO` for Mussoorie. This provides a concise and visually interesting way to look and pollution trends within our Country’s cities.


### Github

Find the link to our code for these visualizations [here](https://github.com/algoasylum/ExploringTheUnseen/blob/master/code/Simpe%20line%20plots.ipynb) 
