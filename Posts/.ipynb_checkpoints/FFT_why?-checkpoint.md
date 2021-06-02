# Does temperature afftect pollutant levels?

Ever wondered the how the pollutant levels change through the day, when does it peak? When is it at its lowest? What is the relationship between temperatue and pollutant levels, if any at all? In this article, we will be exploring and trying to answer the above questions. We will try to visualize this relationship and have look at various methods to describe their relationship. Have a peek at [Pollution Description](https://github.com/algoasylum/ExploringTheUnseen/blob/master/Posts/Pollutants%20Description.md) for a detailed description of pollutants, their acceptable limits and health problems associated with them.

### Data  

The data we use here has hourly readings for various meteorological factors like temperature, humidity, precipitation and pollutant like PM<sub>2.5</sub>, PM<sub>10</sub>, SO<sub>2</sub>, CO etc. The data is available for five Indian cities namely Mumbai, Delhi, Bengaluru, Hyderabad, Jaipur and the availablity is from 2015 - present.

What would be the best way to visualze the relationship between temperature and pollutant levels? Lets start out with simple lineplots to get a feel of what we are working with.

### Lineplot

<img src="../code/images/fftlineplot.png"  width=100% /><br>
Fig1 : Lineplot of Temperature and various pollutants.

Lineplot is one for the most important way to visualize sequential data. They provide us with a fanstastic qualitative representation where it is relatively easy to eyeball trends and relationships within our data. Here, we have plotted temperature and various pollutant readings for Delhi for the first 5 days of December 2019. We can clearly see that temprature increase throughout the day and falls during night, which is to be expected. Interestingly, There also exist a rise and fall pattern in pollutants as well but its rather noisy to draw conclusion. Although lineplots work very well for more obvious trends and patterns, it is rather difficult to make any quantitative conclusions from them. Can we think of a better way to visualize  and quantify the relationship between temperature and pollutants.


### Scatterplot

<img src="../code/images/fftscatterplot.png"  width=90% /><br>
Fig 2 : Scatterplot Temperature vs PM<sub> 2.5 </sub> for Delhi.

On this scatterplot PM<sub>2.5</sub> is plotted against temperature for Delhi for the year of 2019. However, this method fails to present any clear conclusions.

Scatterplot are the obvious choice when we want to study change in one qantity with respect to another, which is what we want to do with temperature and pollutatns. Unfortunately there isn't clear cut relationship between them and scatterplots also do not take time into consideration. So our search continues
### Fourier Transform

<img src="../code/images/fftdelhipm25.png"  width=90% /><br>

fig 3 : FFT (Fast Fourier Transform) of Temperature for Delhi.

What we have learned from lineplots is there are some repeating cycles within our data. So what would happen if we looked at the data from a frequency perspective instead od time. This we enable us to apply Fast Fourirer Transform and decompose our data signals and have a peek at the dominant frequencies and relate them to the time period to which the correspond. For the uninitiated, imagine FFT as a unmixer which can isolate in individual components for a cake batter. Voila! We applied fast fourier transform on hourly temperature reading for Delhi and able able to isolate some distinct frequencies which likely correspond to the repeating patterns we saw in the lineplots. Now we have some dominant frequencies within our temperature data. Lets do the same for pollutants.


<img src="../code/images/fftdelhitemp.png"  width=90% /><br>

Again if we take FFT of hourly PM2.5 readings for Delhi we can can see what appear to the same repeating frequencies as temperatures's FFT. Thus we have found some quantitative realtionship between temperature and pollutant level by experimenting with a bunch of method. In an upcoming post we will take a deeper dive into the fourier transforms and what those dominant frequencies correspond to. Stay tuned!







