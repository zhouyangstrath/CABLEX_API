Basic Operation
===============

Here is an example for how the workflow of CABLEX looks like and the detailed explanation and 
case settings is shown as follows:

Loading Space 1
---------------

You have to create the base model based on the client/TFMC engineers specifications, the base model 
for testing is based on the 800mm Copper Cable and 1000kg Buoy, Detailed info is shown as follows,

::

    Power cable property 	 	        800mm2 Cu
    Outside diameter [mm]		        187.6(SOL)       287.6 (EOL)
    Mass in air [kg/m]		            47.68(SOL)       97.13 (EOL)
    Weight in sea water [N/m]	        439.4(SOL)        NA (EOL)

    Buoy property
    Mass of one buoy	Mb [kg]	        746.56(SOL)      704.30(EOL)
    Net Buoyancy of 1 module	[kg]	1000.0(SOL)      1050(EOL)
    Buoy outer diameter	Db [mm]	        1250.00(SOL)     1250.00(EOL)


The base model **LW_800mm_ESOL.yml** for test run can be accessed by using the following link

.. code-block:: bash

   cd NEV\Floating Offshore Wind\05 Software\CABLEX\CodeSource


Once you have already download the **pc_conf_LS1.py** and **LW_800mm_ESOL.yml** files, make sure they are in the same 
folder, open the VS code, double check the **Design Space** parameters, for test case the parameters range refers to:

::
    
    Water Depth:        79m
    Hang-off possition: 10m
    Layback:            70m:200m:10m
    Total Length:       100m:260m:10m
    Buoy Numbers:       6:21:1 (6,000kg:21,000kg)
    Buoy C to C:        4m, 5m
    1st Buoy Dis:       3m

Open the VS terminal to the exact file path where above two files locates. Modify the DS parameters you wish to change and simply types
to do the case iteration/multiply work for Nominal Position with SOL/EOL Properties.

.. code-block:: bash

    python pc_conf_LS1.py


Testrun1(STATIC PASS): Select LS1/LS2 with default cable configs, 
select Click "Pass Plot Static" to shown the power cable configuration 
info (pass(green tick): not taut, not touching SB/SWL); Tick your checks 
you wish to add on and enter the value you wish to add, i.e., sag/hog clearance 

Testrun2(DYNAMIC PASSS): Select LS4 with default cable configs, select 
Click "Pass Plot Dynamic" to shown the pass configuration(should all pass); 
Tick your checks you wish to add on and enter the value you wish to add, 
i.e., sag/hog clearance and see the updates of pass cases 

Testrun3(CONTOUR PLOTS): Select either LS1/LS2/LS3/L4, chose the params 
you wish to plot at Contours section, Click "Contour Plot" to shown the results


More info needed in this page with v1.4 release with engineers friendly interface