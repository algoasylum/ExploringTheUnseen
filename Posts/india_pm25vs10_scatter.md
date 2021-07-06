 # Particulate Matter in Indian Cities: PM2.5 and PM10

PM (Particulate Matter or particle pollution) is a mixture of solid particles and liquid droplets present in the atmosphere. It comprises of different sizes and can be due to both human and natural sources; primary sources involving automobile emissions,dust and cooking smoke.

Over the past two decades, the concentration of fine particulates increased by 69 percent on average across India. As a result, sustained exposure to particulate pollution now reduces the life expectancy of the typical Indian citizen by 4.3 years compared to 2.2 years in 1998.
For details about pollutants and their consequences refer this [post](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts/Pollutants%20Description.md).

# Generating the Visualization
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

# Visualization Chart - Scatter Plot
## Why Scatter Plots?

Till now, we have mapped our particulate data in the form of line plots. When both variables are quantitative, the line segment that connects two points on the graph expresses a slope, which can be interpreted visually relative to the slope of other lines. However, it is not the ideal choice when observing trends or finding relationship between two variables. While scatter plots also start with plotting quantitative data points, the decision is made that the individual points should not be connected directly together with a line but, instead express a trend. This trend can be seen directly through the distribution of points or with the addition of a regression line. Overall, scatter plots provide the following advantages:
 - It shows the relationship between two variables.
 - It's an ideal method to show a non-linear pattern.
 - The range of data flow, i.e. maximum and minimum values, can be determined.
 - Observation and reading are straightforward.

## Plot Interpretation


<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/sample.html" height="525" width="100%"></iframe>

In the above sample scatter plot, the coordinates of a point (x,y) on the plane represent particulate levels (PM 2.5, PM 10) of that particular instance, specified by its annotation. The color of the point denotes the year and any dotted line joining two points represents the change in levels between corresponding months of given years.

# Observations

### Delhi: India's Gateway and Capital

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Delhi_2020.html" height="525" width="100%"></iframe>

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Delhi.html" height="525" width="100%"></iframe>

## Bengaluru: India's Silicon Valley

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Bengaluru_2020.html" height="525" width="100%"></iframe>

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Bengaluru.html" height="525" width="100%"></iframe>

## Hyderabad: The City of Nizams

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Hyderabad_2020.html" height="525" width="100%"></iframe>

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Hyderabad.html" height="525" width="100%"></iframe>

## Kolkata: The City of Joy

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Kolkata_2020.html" height="525" width="100%"></iframe>

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Kolkata.html" height="525" width="100%"></iframe>

## Mumbai: The Commercial Capital

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Mumbai_2020.html" height="525" width="100%"></iframe>

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://abhishek-1131.github.io/plotly-plots/Mumbai.html" height="525" width="100%"></iframe>
