# Stellar Motion
The star spectrum data in the spectra matrix was collected at evenly spaced wavelengths (λ), and you are given the starting wavelength (λstart), the spacing (λdelta), and the number of observations.
## Step 1
Create a variable named lambdaEnd (λend) that contains the value of the last wavelength in the recorded spectrum. You can calculate lambdaEnd with the expression λstart+(nObs−1)λdelta.
Use lambdaEnd to create a vector named lambda λ) that contains the wavelengths in the spectrum, from λstart to λend, in steps of λdelta.
## Step 2
Each column of spectra is the spectrum of a different star. The sixth column is the spectrum of star HD 94028.
Extract the sixth column of spectra to a vector named s.
## Step 3
Plot the spectra (s) as a function of wavelength (lambda). Use point markers (.) and a solid line (-) to connect the points.
Add the x-label "Wavelength" and the y-label "Intensity" to the plot.
## Step 4
Recall that the min function allows two outputs, the second of which is the index for the minimum value. This index corresponds to the location of the hydrogen-alpha line (λHa).
Create two variables, sHa and idx, that contain the minimum value of s and the index of that minimum value. Find the wavelength of the hydrogen-alpha line by using idx to index into lambda. Store the result as lambdaHa (λHa).
## Step 5
The point (lambdaHa,sHa) is the location of the hydrogen-alpha line. Add a point to the existing axes by plotting x = lambdaHa, y = sHa as a red square ("rs") with a marker size (MarkerSize) of 8.
## Step 6
If you zoom in on the plot, you can see that the wavelength of the hydrogen-alpha line of HD 94028 is 656.62 nm, which is slightly longer than the laboratory value of 656.28 nm. Using the hydrogen-alpha wavelength of the star, you can calculate the redshift factor (the speed of the star relative to Earth) using the formula z=(λHa/656.28)−1.  You can then calculate the speed by multiplying the redshift factor (z) by the speed of light (299792.458km/s). 
Calculate the redshift factor (z) and the speed (in km/s) at which the star is moving away from Earth. Assign the redshift factor to a variable named z and the speed to a variable named speed.

