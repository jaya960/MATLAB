# Project 1 - Stellar Motion
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

## First Observation
![image](https://github.com/user-attachments/assets/8330b77f-209d-460d-809f-7f568df56668)

where, <br>
sHa -> Minimum Intensity of HD94028 or Intensity at Hydrogen-Alpha line <br>
idx -> Index of the minimum intensity in the spectrum of HD94028 <br>
lambdaHa -> Wavelength of HD94028 at Hydrogen-Alpha line <br>

## Second Observation
![image](https://github.com/user-attachments/assets/ff9e83c4-ff42-491a-8469-c007a7d9fe58)

Spectrum of HD94028

## Third Observation
![image](https://github.com/user-attachments/assets/45c5485c-5480-46d2-8881-439117f2fb70)

where, <br>
z -> red-shift factor of HD94028 star <br>
s -> speed of HD94028 (km/s) <br>

## Conclusion

HD94028 star is moving away from the earth at a speed of 155.3139 km/s


# Project 2 - Compare Stellar Spectra
In the previous project, I calculated the speed (in km/s) of a star relative to Earth by using its spectrum. In this project, I will calculate all the stars' speeds at once. Then I'll create a plot of the star spectra.

# Step 1
Extract the spectrum data for the each star in the matrix spectra. Then calculate the speed based on that data. How would you calculate the speed of all the stars in spectra?
You could repeat the calculations in a for loop, but it is more efficient to use array operations instead.

# Step 2
Notice that speed is now a vector. A positive speed means that the star is moving away from Earth (redshifted spectrum), and a negative speed means that the star is moving toward Earth (blueshifted spectrum).
In the next few steps, you'll plot the spectra of all seven stars using different line properties for redshifted and blueshifted spectra. It is convenient to use a for loop to access each star's data one at a time.
Create a for loop with a loop index named v. The loop index should progress through all columns of spectra (1 to 7).
In the loop body, extract the vth column of spectra to a variable named s.

# Step 3
You can use an if statement to differentiate between redshifted and blueshifted spectra.
First, you'll plot the blueshifted spectra using dashed lines.
Add an if statement to the for loop body. If speed(v) is less than or equal to 0, create a plot of s against lambda using a dashed line (--).
Add the command hold on between the two end keywords so that you only create one plot.

# Step 4
Now you'll plot the redshifted spectra using thick lines.
Add an else statement. If speed(v) is greater than 0, create a plot of s against lambda using a line width of 3.
After the for loop, enter hold off.

# Step 5
You can pass text directly to the legend function.
The string array starnames contains the name of each star in spectra.
Add a legend to the plot using the array starnames.

# Step 6
In the plot, you identify stars with redshifted spectra by using their line styles, and then look up their names in the legend. Can you determine the names of the redshifted spectra without a for loop?
Recall that you can use logical indexing to find elements that match a condition.
c = b(a < 6)
Create a variable movaway that contains the elements in starnames corresponding to where speed is greater than 0.

# Step 7
Like many functions in MATLAB, plotting functions can accept matrix inputs. plot(A) creates a line for each column in A.
If you do not want to differentiate between redshifted and blueshifted spectra, you do not need to use a for loop.
You can simply use: <br>

      plot(lambda,spectra) <br>
      
      legend(starnames)

# First Observation
![image](https://github.com/user-attachments/assets/b5eca75a-ab27-4e01-8aab-853851512f11)

where, Speed is a vector

# Second Observation
![image](https://github.com/user-attachments/assets/6601b299-f5b9-4971-9d10-2ee62789d2f4)

Spectra of all the 7 stars in starData

# Third Observation
![image](https://github.com/user-attachments/assets/8db1a08e-1721-47fb-a9f0-132a51e33286)

Names of the Red-Shifted Spectra (Obtained from Step 6)

# Fourth Observation
![image](https://github.com/user-attachments/assets/fd3328ff-7151-4381-9a83-3096bb7ff1d4)

Spectra obtained from the last step






