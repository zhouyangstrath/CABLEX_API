Introduction
============

#README

Tool Name: CABLEX (technipFMC power CABLE EXcellence Optimisation)
Version: 1.2.0 (Static & Dynamic) Test Version
Author Name: Yang Zhou (yang.zhou@technipfmc.com/careers@yzhou.uk)

####################################
Introduction: Preliminary design check for floating offshore wind power cables with multiple cable configurations and loading spaces

Key Features:
1. Preliminary Power Cable Inspection 
2. User Friendly Results Visualisation
3. Flexible Check Range Availability 
4. Optimised Cable Configuration Exportations 

####################################

####################################	        
Power Cable Configuration:
		    
		Fairlead
	    	  |\         Hog
	    	  | \        /~\~ Buoy
	   	  |  \      /~  \~
WaterDepth = 79m  |   \    /~    \~   TotalLength(PC)
	   	  |    \  /       \
	   	  |     \/         \
	    	  |    Sag          \    
	     _____|__________________\______________ 
                        LayBack      Anchor

5 Key Parameters:
LayBack # LayBack
Total Length: # Power Cable Total Length
Buoy:  # Buoy Uplift
Buoy_CC: # Buoy to Buoy Distance, 1m for buoy diameter actual distance is Buoy_FF+1
1st Buoy: # Anchor to 1st Buoy Distance
####################################
Cable: 300mm; 800mm(current example)
Buoy: 300kg; 1000kg(current example)
####################################
Usage:
• No Need for installation, double click "CABLEX.exe", it may take 60s for the User Interface to open.
• Please use "reset plot" button after each contour plot selection 

####################################
#DATA SOURCE#
Offsets:
Norminal: 0% WaterDepth fairlead displacement 
Near/Far/Cross: 30% WaterDepth fairlead displacement 

Marine Growth:
SOL: Start of life
EOL: End of life

Loading Space:
LS1(first step): rough static check with wide range of Layback/TotalLength/Buoy
LS2(second step): detailed static check with offsets based on finer configurations obtained from the pass cases(not taut and SAG/HOG not touching SB/SWL) from LS1
LS3(third step): more detailed static check with offsets/current based on the pass cases from LS2 (SAG/HOG clearance 15% water depth)
LS4(fourth step): general dynamic check with specified time domain series for powercable fairleadpoint (50-y return period)

#####################################
#Flexible Checks Selection
[S/D]: apply to static & dynamics
[D]: apply to dynamic only
[S]: apply to static only

#####################################
#TEST RUNS#
  Testrun1(STATIC PASS): Select LS1/LS2 with default cable configs, select Click "Pass Plot Static" to shown the power cable configuration 
			  info (pass(green tick): not taut, not touching SB/SWL); 
			  Tick your checks you wish to add on and enter the value you wish to add, i.e., sag/hog clearance 
  Testrun2(DYNAMIC PASSS): Select LS4 with default cable configs, select Click "Pass Plot Dynamic" to shown the pass configuration(should all pass); 
			   Tick your checks you wish to add on and enter the value you wish to add, i.e., sag/hog clearance and see the updates of pass cases 
  Testrun3(CONTOUR PLOTS): Select either LS1/LS2/LS3/L4, chose the params you wish to plot at Contours section, Click "Contour Plot" to shown the results

####################################

####################################
Appendix for Functions Introduction:
  Select Data Source: 
	Select the data you would like to visualise at different offsets
  Select Two Parameters & Fixed Parameters:
	Provide you with the data information you select for 2D slice X axis: selected_para1 Y axis: selected_para2
	other three parameter fixed based on the inputs
  Contour Plot source:
	Source used for Contour Plot Button: Avail: Top/Bottom Tension; Top Angle; SAG/HOG Radius; Cost
  Pass Contour Plot source(Static only yet):
	Source used for Pass Contour Plot Button: Avail: Top/Bottom Tension Difference between N/F; Top Angle Difference N/F
####################################

Contact:
If you got any questions or comments, feel free to contact yang.zhou@technipfmc.com 


