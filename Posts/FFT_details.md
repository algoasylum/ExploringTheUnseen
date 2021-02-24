# Exploring Fourier Transforms

In the previous post we tried, to explore the relationship between temperature and pollutant level using various method and ended up with Fourier Transforms as the best way to visualize and quantify the above mentioned relationship.

### Data  

The data we use here has hourly readings for various meteorological factors like temperature, humidity, precipitation and pollutant like PM<sub>2.5</sub>, PM<sub>10</sub>, SO<sub>2</sub>, CO etc. The data is available for five Indian cities namely Mumbai, Delhi, Bengaluru, Hyderabad, Jaipur and the availablity is from 2015 - present.

### Fourier Transforms

To put it simply, Fourier Transforms takes in time-based data/pattern, tries to decomposes it in a bunch of sine waves and returns the frequency and the amplitude of the same. It is similar to extracting ingridients from a dish.

<img src="../code/images/fftdelhitemp.png"  width=100% /><br>
fig 1 : FFT (Fast Fourier Transform) of Temperature for Delhi.

Taking the fourier transform we can see, two distinct frequency with significant amplitude. Let us explore which frequencies might these be?

<img src="../code/images/fftdelhitempfreq.png"  /><br>

Examining further, the frequency which maximum amplitude is 0.00014 i.e 1 / 365 * 24. This corresponds with the yearly variation of temperature which is expected. The second dominant frequency is 0.0416 i.e 1/24, corresponding to the daily variation in our temperature. Thus, temperature seems to follow a yearly and a daily trend evident from the Fourier transform. Now lets explore the same thing for PM <sub>2.5</sub>.

<img src="../code/images/fftdelhipm25.png"  width=100% /><br>
fig 1 : FFT (Fast Fourier Transform) of PM<sub> 2.5 </sub> for Delhi.

We again see similar dominant frequencies for PM<sub> 2.5 </sub> as well. But overall there are a large number of non-dominant frequencies present as well attributed to the greater flucations of PM<sub>2.5</sub> readings.

<img src="../code/images/fftdelhipm25freq.png"  /><br>

The most dominant frequency is the same as the temperature one i.e 0.00015 = 1 / 365 * 24, corresponding the yearly variation. Thus PM<sub> 2.5 </sub> also follows the yearly pattern. More interestingly the following dominant frequency are half-yearly and quater-yearly. Again, 0.0416 = 1 / 24 shows up, the daily frequency. Thus, there exists a yearly and daily realtionship between Temperature and PM<sub>2.5</sub> and this is shown elegantly by FFT.

### Fourier Transform for other cities.

<img src="../code/images/fftall.png"  /><br>

### Conclusion
.....


