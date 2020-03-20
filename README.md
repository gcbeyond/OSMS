# Open-Source Miniature Spectrophotometer (OSMS)
*The OSMS software was designed by Katrina Laganovska, University of Latvia, Institute of Solid State Physics (www.lum.lv). 
If you have any questions, comments or feedback, please contact me at katrina.laganovska@cfi.lu.lv. or here*
## The complete and updated software 

### Short guide to everything:

The ready-to-use software files can be found in the release section and the source files have been uploaded here. 

**To use the device without making changes:**
1. Assemble the device
2. Upload Arduino code to your Arduino microcontroller
3. Install Android app or run the Python software

**How to measure the absorption spectrum:**
1. Connect to Bluetooth if using app (you'll need to pair your HC-05 module with your phone first)
2. Measure the baseline (the spectrum of the LED wihtout the sample in)
3. Insert sample
4. Choose either "Single" or "Continuous" measurement in Desktop mode or "Capture" in the Android app. 
5. Repeat from step 2 for additional samples (however it is recommended to re-measure the baseline every once in a while)

Notes: 
* Accumulation and continuous measurements are only possible in Desktop mode
* The STOP button will halt the continuos process only after finishing the running measurement. 
* When changing accumulation time, make sure to measure the baseline again. 
* In order to save continuos measurements as a series of files, enable lines 292 and 293 and disable 295. 
______________________________________________________________________________________________

### For users who want to customize the software/device:


See the commented Arduino code. Simple test functions have been left in the code (turning the built-in LED of the Arduino on and off for the purpose of troubleshooting). 

LED:
In the final version the LED turns on automatically whenever the device is turned on, however, for testing purposes, that can be changed in the Arduino code. This allows to measure dark noise or just check if the commands are going through. Additionally a block of code for automatic LED brightness calibration has been left in, if the user finds it would suit his needs better (however, it slows down the process considerably). 

Baseline spectrum and the spectrum (when a sample is inserted) are saved automatically when used in Desktop mode (baseline.txt and spectrum.txt respectively) and can be viewed for calibration purposes (exposure time/LED brightness setting combination).  



