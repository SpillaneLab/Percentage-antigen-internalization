# Percentage-antigen-internalization
Fiji macros that can be used to reslice and max-project cells to visualize internalization and determine percent antigen internalization. 

# Overview 
Please read our Methods Chapter (reference to come) on the experimental setup to investigate antigen internalization. A common way to analyze the efficiency of B cell antigen internalization is to quantify the percentage of available antigen that B cells internalize from the immune synapse (1, 2). This can be determined by measuring the antigen fluorescence intensity in the cell (above the synapse plane), and dividing it by the total antigen fluorescence intensity in the cell and in the synapse (Figure 1). <br/> <br/>
![Picture1](https://github.com/SpillaneLab/Percentage-antigen-internalization/assets/143707918/01ae2dca-4f03-468b-8d7f-0c3610257f1f) <br/> <br/>
Figure 1. (A) Maximum intensity projections of a naive B1-8 B cell that was plated onto planar lipid bilayer coated with NIP-coupled DNA sensors, fixed after 45 minutes, and stained for surface (B220) and intracellular (phospho-myosin light chain, pMLC) markers. (B) Schematic showing the distribution of internalized antigen located inside the cell, and total antigen in the cell and in the synapse. (C) Using Otsu thresholding, we generate masks using the B220 signal to define the "cell" and “cell + synapse" regions of interest, and overlay the masks onto the Atto647N signal. (D) The extracted Atto647N signal intensities are used to quantify the percentage of antigen internalized using the equation given in (B). Scale bars, 5 µm. 

# Installation 
Analysis performed using Fiji (https://imagej.net/software/fiji/). 
1.	Copy the code (from browser or download as .txt) and paste into macro window as: 
     Plugins > New > Macro
2.	Ensure the language is set to IJ1 Macro in the Language tab of the macro window. 
3.	Save the macro using .ijm extension. 
# How to use 
1.	Run macros from “get cell crops” repository, using either a membrane stain or the brightfield channel. Thresholding parameters should be adjusted accordingly, and cell crops can be obtained manually if this macro does not work. 
2.	Run the “reslice” macro to reslice the Z-stack image. 
3.	Run the “maximum projection” macro to create a maximum projection of the resliced image. This generates a side view of the B cell that can be used to visualize antigen internalization. 
4.	The user should then manually crop around the “cell” and “cell + synapse” as shown in Figure 1 and use the “automated segmentation” macro (adjusting parameters as appropriate) for segmentation. We recommend segmenting on a membrane stain, such as B220, as shown in Figure 1. To determine the percentage of antigen internalized, the intensity of the “cell” should be divided by that of the “cell + synapse” and multiplied by 100.
   
Cell crop and automated segmentation macros are given in other repositories available on our Github page. 

# References 
1. Nowosad CR, Spillane KM, Tolar P. Germinal center B cells recognize antigen through a specialized immune synapse architecture. Nature Immunology. 2016;17(7):870-7.
2. Spillane KM, Tolar P. B cell antigen extraction is regulated by physical properties of antigenpresenting cells. Journal of Cell Biology. 2017;216(1):217-30.
