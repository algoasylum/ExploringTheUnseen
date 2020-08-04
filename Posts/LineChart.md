# Pollution in Indian Cities: Lockdown 
The lockdown has led to a pause in most economic activities – manufacturing and construction has ground to a halt and there are no vehicles on the road. There are numerous instances of how this has led to a reduction in environmental pollution, and in this article, we try to make visualize the
scale and rate of what happened.

The major components of air pollution are `particulate matter of sizes 2.5 microns and 10 microns` in width (PM2.5 and PM10 respectively), and gases such as `Carbon Monoxide` (CO), `Nitrogen Dioxide` (NO<sub>2</sub>), `Sulpher Dioxide` (SO<sub>2</sub>) `Ozone` (O<sub>3</sub>).

# Generating the Visualization
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

<img src="../code/images/pm2.5_barchart.png"  height=500 width=1200 /><br>
Fig 1 : PM2.5 values for 7 Indian cities represented as a Bar Chart<br>

In this article we plot line and bar charts of various pollutants for 7 cities, across India. Here dates are plotted on X axis and `Y axis` represents the `median values of pollutants` observed over a 24-hour frame.<br>


# Observations 
### Lets plot few cities

<img src="../code/images/pm2.5_line_chart_3.png"  height=500 width=1200 /><br>
Fig 2 : PM2.5 values for Delhi, Kolkata, Mumbai as line chart. Here the `Green` Line represents `NAACQ` standards and `Yellow` Line represents `WHO` standards.

Few details are very evident from `Fig 1` and `Fig 2`. Delhi is the most polluted  of all the cities. All the cities show reduction in PM2.5 level as we move from March to July, and our initial assumption is that this is due to the lockdown – there is a significant drop after March, which is when the country went into lockdown. In Fig2, Green and yellow lines represent WHO and NAACQ recommended levels. It is only after lockdown we see Mumbai and Kolkata’s level below NAACQ but higher than WHO. Delhi stills seems to be above all recommendations.

### Focus on Mumbai
<img src="../code/images/pm2.5_mumbai.png"  height=500 width=1200 /><br>
Fig 3: PM2.5 values for Mumbai.

Consider Mumbai for example, which shows significant drop in PM2.5 as we move from January to July falling well under NAACQ guidelines after lockdown even under WHO in some cases. Other cities show similar trends as well with some outliers in Bengaluru and Chennai.

### PM2.5 for all cities
<img src="../code/images/pm2.5_all_cities.png"  height=500 width=1200 /><br>
Fig 4: PM2.5 values for all the cities.
### Plot them all!
<img src="../code/images/all_pollutants.png"   width=100% /><br>
Fig 5: All the polltants for every city.
# Conclusion
As we move from January to July most cities show significant reduction in their PM2.5 and PM10 levels after March i.e when lockdown was imposed. Cities like Delhi with high pollution levels show reduction, but plateau out after some time, while cities like Mumbai and Kolkata show reduction in their pollution leevels. But these are not without some outliers i.e peaks in Bengaluru and Chennai. This provides a concise and visually interesting way to look and pollution trends with our Country’s major cities.

### Github

Find the link to our code for these visualizations [here](https://github.com/algoasylum/ExploringTheUnseen/blob/master/code/Simpe%20line%20plots.ipynb) 





 