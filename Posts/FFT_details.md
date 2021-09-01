# Exploring Fourier Transforms

In the previous post we tried, to explore the relationship between temperature and pollutant level using various method and ended up with Fourier Transforms as an interesting way to visualize and quantify the above mentioned relationship.

### Data  

The data we use here has hourly readings for various meteorological factors like temperature, humidity, precipitation and pollutant like PM<sub>2.5</sub>, PM<sub>10</sub>, SO<sub>2</sub>, CO etc. The data is available for five Indian cities namely Mumbai, Delhi, Bengaluru, Hyderabad, Jaipur and the availablity is from 2015 - present.

### Fourier Transforms

To put it simply, Fourier Transforms takes in time-based data/pattern, tries to decomposes it in a bunch of sine waves and returns the frequency and the amplitude of the same. For the uninitiated, FFT is akin to extracting individual ingredients from a cake batter.

<img src="../code/images/fftdelhitemp.png"  width=100% /><br>
fig 1 : FFT (Fast Fourier Transform) of Temperature for Delhi.

Taking the fourier transform we can see, two distinct frequency with significant higher amplitudes than the other frequencies. Let us explore which frequencies might these be and to what time period do they correspond?

<img src="../code/images/fftdelhitempfreq.png"  /><br>

Examining further, the frequency which maximum amplitude is 0.000114. We know that time is `1/frequency`, so `1 / 0.000114 = 8771` which is approximately equal to  `1 / 365 * 24`. This corresponds with the yearly variation of temperature which is expected. The second dominant frequency is 0.04167, and following the same methods a above the time period comes out to be 24 (1 / 0.041667), corresponding to the daily variation in our temperature. Thus, temperature seems to follow a yearly and a daily trend evident from the Fourier transform. Now lets explore the same thing for PM <sub>2.5</sub>.

<img src="../code/images/fftdelhipm25.png"  width=100% /><br>
fig 1 : FFT (Fast Fourier Transform) of PM<sub> 2.5 </sub> for Delhi.

We again see similar dominant frequencies and multiples of these dominant frequencies for PM<sub> 2.5 </sub> as well. But overall the amplitude of other of frequencies present in the PM<sub>2.5</sub> data is higher due to the greater flucations of PM<sub>2.5</sub> readings.

<img src="../code/images/fftdelhipm25freq.png"  /><br>

The most dominant frequency is the same as the temperature one i.e `0.00015 = 1 / 365 * 24`, corresponding the yearly variation. Thus PM<sub> 2.5 </sub> also follows the yearly pattern. More interestingly the following dominant frequency are half-yearly and quater-yearly. Again, 0.0416 = 1 / 24 shows up, the daily frequency. Thus, there exists a yearly and daily realtionship between Temperature and PM<sub>2.5</sub> and this is shown elegantly by FFT.

### Fourier Transform for other cities.

<img src="../code/images/fftall.png"  /><br>

### Conclusion
We looked at the relationship between temperature and pollutants using Fourier Transform. We also explored the dominant frequencies and saw an annual and daily variation.



