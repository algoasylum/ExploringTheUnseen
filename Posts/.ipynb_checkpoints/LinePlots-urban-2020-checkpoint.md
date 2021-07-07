# Pollution in Indian Cities: Lockdown 
The lockdown has led to a pause in most economic activities – manufacturing and construction has ground to a halt and there are no vehicles on the road. There are numerous instances of how this has led to a reduction in environmental pollution, and in this article, we try to make visualize the
scale and rate of what happened.

The major components of air pollution are `particulate matter of sizes 2.5 microns and 10 microns` in width (PM2.5 and PM10 respectively), and gases such as `Carbon Monoxide` (CO), `Nitrogen Dioxide` (NO<sub>2</sub>), `Sulpher Dioxide` (SO<sub>2</sub>) `Ozone` (O<sub>3</sub>). For details about pollutants and their consequences refer this [post](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts/Pollutants%20Description.md).

World Health Organisation (WHO) and National Ambient Air Quality Standards (NAAQS) have their standards to keep pollution in check, we incorporate these in all our plots.

# Generating the Visualisation
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

### The Overall trend
<img src="../code/images/pm2.5_barchart.png"  /><br>
`Fig 1` : PM2.5 values for 7 Indian cities represented as a Bar Chart<br>

This figure shows `Stacked Bar Chart` of daily median values for `PM2.5` across various cities. This gives a high-level overview of the trends across the cities in a single chart. X axis is Dates and Y axis represents median values of pollutants calculated over a 24-hour frame. We observe higher values in January and February and after March we start to the reduction in the pollutant levels probably due to Lockdown imposed after Covid-19. Overall levels pretty much remain the same from April to July with few peaks and dips. <br>


# Line Plots

Line plots are intuitive way of interpreting how a particular parameter (dependent variable) varies with change in another(independent variabl). Usually the independent variable is plotted on X-axis and dependent on Y-axis. Here we study changing PM2.5 levels as time progresses, we look at a particular date and the Y-axis represents the PM2.5 levels at that point in time. This simple yet very powerful tool gives quick and incredibile insights in the trends/patterns observed within our data.

### Lets plot few cities

<img src="../code/images/pm2.5_line_chart_3.png"  /><br>
`Fig 2` : PM2.5 values for Delhi, Kolkata, Mumbai as line chart. Here the `Green` Line represents `NAAQS` standards and `Yellow` Line represents `WHO` standards.

Few details are very evident from `Fig 1` and `Fig 2`. Delhi is the most polluted of all the cities and starts out with huge levels of PM2.5. All the cities show reduction in PM2.5 level as we move from March to July, and our initial assumption is that this is due to the lockdown – there is a significant drop after March, which is when the country went into lockdown. In Fig2, Green and yellow lines represent WHO and NAAQS recommended levels. It is only after lockdown we see Mumbai and Kolkata’s level below NAAQS but higher than WHO. Delhi stills seems to be above all recommendations.

### Focus on Mumbai
<img src="../code/images/pm2.5_mumbai.png"   /><br>
`Fig 3`: PM2.5 values for Mumbai.

Consider Mumbai for example, which shows significant drop in PM2.5 as we move from January to July falling well under NAAQS guidelines after lockdown even under WHO in some cases. Mumbai shows two major dips between January and February and spike in mid-March. These maybe due to errors in obeservation or some other factors unknown to us at this point. Other cities show similar trends as well with some outliers in Bengaluru and Chennai.

### PM2.5 for all cities
<img src="../code/images/pm2.5_all_cities.png"  width=100% /><br>
`Fig 4`: PM2.5 values for all the cities.

Clearly Delhi is most polluted here, followed by Kolkata and Mumbai. Most of the cities show reduction in PM2.5 levels around March-April buffer, in accordance to the initial lockdown assumption. After lockdown, all cities but Delhi fall below the NAAQS standards but still above the WHO guidelines. If we take a closer look at Chennai after the May period the PM2.5 levels show steady increase.
### Plot them all!
<img src="../code/images/all_all_cities_trans.png"   width=100% /><br>
`Fig 5`:All the polltants for every city.

Here every row represents a Pollutant and every column a City for better comparision across the board.

Taking a look at PM10 levels again we see Delhi leading the PM10 levels folowed by Kolkata. We see reduction in PM10 levels for these cities after March. Kolkata's PM10 starts above Indian standards but as we reach July it is already before WHO guidelines, a good improvement. Hyderabad, Chennai and Mumbai have relatively low levels of PM10 to begin with, already under Indian standards and towards July fall under WHO standards as well. Chennai seems to have PM10 data missing for the month of May. 

### Lets take a transpose.

<img src="../code/images/all_pollutants.png"   width=100% /><br>

`Fig 6`: All the polltants for every city [Transpose].

Every row represents a City and every column a pollutant, just another way to look at things.

Taking a look at `CO` levels Delhi, Kolkata and Mumbai are topping the CO charts. We see some level of reduction in CO levels across all cities except Chennai. However, all the cities are well above the Indian standards even after lockdown!

For `SO2` levels Delhi, Kolkata and Mumbai are equally polluted. Reduction on a small level is seen after May. Bengulru's SO2 levels are overall consistent throughout.

`NO2` here Kolkata beats Delhi for the most polluted crown. Mumbai and Kolkata show a signficant amount of improvement in their NO2 levels. Delhi, Bengaluru and Hyderabad also show reduction. Chennai however shows consistent NO2 levels.


# Conclusion
As we move from January to July most cities show significant reduction in their PM2.5 and PM10 levels after March i.e when lockdown was imposed. Cities like Delhi with high pollution levels show reduction, but plateau out after some time, while cities like Mumbai and Kolkata show reduction in their pollution levels. But these are not without some outliers i.e peaks in Bengaluru and Chennai. This provides a concise and visually interesting way to look and pollution trends within our Country’s major cities. Whether the reduction in pollutant levels is strictly due to Lockdown or other factors is unknown to us at this point. We will investigate factors like seasonal influence in an upcoming article. Stay tuned!

### Github

Find the link to our code for these visualizations [here](https://github.com/algoasylum/ExploringTheUnseen/blob/master/code/Simpe%20line%20plots.ipynb) 





 
