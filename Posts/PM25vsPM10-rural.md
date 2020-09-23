# Particulate Matter in Indian Cities(II): Exploring Diversity

In the previous post, we took a look at the PM (Particulate Matter) levels in major cities like Mumbai, Delhi, Bengaluru, Chennai, Kolkata and Visakhapatnam.In this post, we focus on the PM levels of some of the lesser developed cities namely `Guwahati`, `Coimbatore`, `Jabalpur`, `Kota`, `Mussoorie`, `Vapi` to see their trends in pollution levels as lockdown due to COVID is gradually lifted.

PM (Particulate Matter or particle pollution) is a mixture of solid particles and liquid droplets present in the atmosphere. It comprises of different sizes and can be due to both human and natural sources. While PM 2.5 is mainly produced due to common indoor activities involving tobacco smoke, cooking and burning, PM 10 

Over the past two decades, the concentration of fine particulates increased by 69 percent on average across India. As a result, sustained exposure to particulate pollution now reduces the life expectancy of the typical Indian citizen by 4.3 years compared to 2.2 years in 1998. 
For details about pollutants and their consequences refer this [post](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts/Pollutants%20Description.md).

# Generating the Visualization
The AQI values for these cities was obtained from [AQICN](https://aqicn.org/data-platform/) in csv format containing values corresponding to multiple gases for major cities around the globe. Data was loaded into a pandas dataframe in order to extract values corresponding to cities under consideration (in the Indian subcontinent), followed by cleaning and formatting of data in order to incorporate correct date format and resolving discrepancies.
The processed data was passed to the [Plotly graphing library](https://plotly.com/) in order to generate a scatter plot, highlighting the information present.

# Observations
## Guwahati: The gateway to the Northeast

<img src="../code/images/pm25vspm10_rural/guwahati.png"  width=100% /><br>

In the above figure:
- Changes in the levels of particulate matter for Guwahati are plotted over a period of 7 months (Jan 2020 to July 2020).
- Co-ordinates of a point (x,y) represent the PM2.5 and PM10 values for the month respectively. 
- The month-wise temporal trend for both the PM values can be understood by traversing the line, starting from the vertex labelled Jan till the last vertex (July).

While having relatively higher values of particulate matter compared to other mentioned cities, Guwahati observes a steady decline in the PM 2.5 and PM 10 levels as we move from January to July. The decline is accelerated post March, possibly owing to the initiation of the lockdown in March, due to COVID-19.

## Coimbatore : Manchester of South India (Textile Industry)

<img src="../code/images/pm25vspm10_rural/coimbatore.png"  width=100% /><br>

While the general decreasing trend of particulate matter levels is prevalent, the PM10 values actually rise from April to May, while the PM 2.5 levels continue to decline. However, the transition from June to July notices a spike in both the values, possibly owing to the relaxation of restrictions placed due to the lockdown.

## Jabalpur : Cultural capital of Madhya Pradesh 

<img src="../code/images/pm25vspm10_rural/jabalpur.png"  width=80% /><br>

The presence of a sharp decline in PM levels from Feb to Mar followed by a relatively small reduction and almost no change in PM10 values over the next couple of months, is quite interesting to observe, given that the lockdown got imposed in Mar itself. This is followed by a subsequent decline in the levels over the next couple of months.

## Kota : India's education factory (Rajasthan)

<img src="../code/images/pm25vspm10_rural/kota.png"  width=100% /><br>

Apart from a short spike in PM 2.5 levels from April to May, Kota observes a consistent decline in PM levels (Feb onwards).

## Mussoorie : Queen of the Hills (Uttarakhand)

<img src="../code/images/pm25vspm10_rural/mussoorie.png"  width=100% /><br>

Unlike other places covered previously, Mussoorie observes a huge spike in particle pollution levels from Jan to Feb and from April to May, followed by huge declines in levels in the coming months.

## Vapi : Popular industrial hub (Gujarat)

<img src="../code/images/pm25vspm10_rural/vapi.png"  width=100% /><br>

Fairly linear and consistent reduction in levels of particulate matter from the start of the year to July.





