# Activity-Localization-Imaging

This folder contains MATLAB routines that demonstrate Activity Localization Imaging (ALI). 

A Python implementation of ALI developed by Dr. Urs Böhm is available at:
https://github.com/spinaldynamicslab/pyALI

A small voltage imaging dataset is provided in the 'ali_demo_data.mat' file.
This dataset contains images of mouse CA1 neurons expressing the voltage indicator 'Voltron 2'.
These cells were imaged in vivo at 2000 frames per second using a high speed camera.
In these images, neuronal spiking can be seen as brief decreases in fluorescence intensity. 

Installation:
-----------------------------------------------------------------------
(1) Decompress all files in the provided .zip file into a target folder.

(2) Run MATLAB and add the target folder along with its subfolder into the MATLAB search path. 

(3) Run demo_script.m by typing 'demo_script' in the Command Window and press Enter.

Function:
-----------------------------------------------------------------------
The demo_script.m uses the provided functional m-files to do the following tasks:

(1) Load the example data, perform pixelwise high-pass filtering to create df images

(2) Detect and localize spikes

(3) Generate an ALI map from the resulting spike coordinates

(4) Automatically detect spike clusters from the ALI map

(5) Calculate footprints and extract traces

The demo_script generates 2 figures. The expected results are shown in the provided 'expected_result.pdf' file. 

The expected run time on a standard desktop computer is 10 seconds.

System requirement: 
-----------------------------------------------------------------------
The codes have been tested on a standard desktop PC running Windows 11, MATLAB 2022b with the following toolboxes
Signal Processing Toolbox (medfilt.m)
Image Processing Toolbox (bwconncomp.m ; imregionalmax.m ; fspecial.m )
Statistics and Machine learning Toolbox (mad.m)
