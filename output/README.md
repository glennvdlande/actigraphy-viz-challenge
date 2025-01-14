Submission to ADVAnCe - Actigraphy Data Visualization and Analysis Challenge by Glenn van der Lande.

This folder contains the figures generated by the code.

Figures contain 3 parts. The upper subplot contains the daylight where white is a period of daylight and black a period of darkness. 
Daylight is calculated based on the dates and location of the actigraphy recording. Between sunrise and dawn and dusk and sunset, light levels increase/decrease linearly.
The middle part contains the light exposure as measured by the actigraphy device, with the same color code. 
The bottom figure contains the raw actigraphy data with the counts on the left y-axis and dates on the x-axis. Note that the light subplots share the same x-axis. 
The right y-axis contains periods in 4-hour bins (except the first 0-2 hour bin, which is odd because it often contains noise). 
Singular Spectrum analysis was applied to the data to decompose the signal in rhythms and extract their importance. 
This is a data-driven approach that allows the investigation of circadian and ultradian rhythms. 
Moreover, it allows for day-to-day variations in strength and frequency of the rhythm, making it a suitable tool to investigate variations.
Accordingly, we reconstruct the 10 most important rhythms (note that his can be changed in the code) and determine their period and relative strength.
Then we normalize the reconstructed signal between 0 and 1, multiply it with its weight, add multiple competing rhythms in the same bin together and plot this as a heatmap.
Thus, the intensity of the heatmap displays the relative strength of rhythms in a bin and its pattern (blurred, clearly defined, etc.) hints at the integrity of the rhythm.
With the addition of the Zeitgeber, light, in the top plots, we can see in an instant if the subject adheres to a strong circadian rhythm or not, and how this corresponds to the light exposure.
Moreover, less strong or more fragmented circadian rhythms, and stronger ultradian rhythms may be signs of pathology that can be detected easily, on an individual subject basis.

