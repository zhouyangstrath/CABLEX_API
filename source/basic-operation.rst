Basic Operation
===============

Here is a show case for how the workflow of CABLEX looks like and the detailed explanation and 
case settings is shown as follows:

Loading Space 1
---------------

The aim of LS1 is to find out the basic green zone for lazywave configurations design with no offsets(Norminal),

**Details of LS1**
::

    Static
    Nominal 
    No offsets
    No current

For a lazywave shape, the following Design Space Parameters is considered,

**Details of DS1**
::

    Layback:            70m:200m:10m
    Total Length:       100m:260m:10m
    Buoy Numbers:       6:21:1 (6,000kg:21,000kg)
    Buoy C to C:        4m, 5m
    1st Buoy Dis:       3m


1. **BASE MODEL CREATION:** Create the base model based on the client/TFMC engineers specifications, the base model 
for the show case is based on the 800mm Copper Cable and 1000kg Buoy as a shown case, Detailed info presented as follows,

::

    Power cable property 	 	        800mm2 Cu
    Outside diameter [mm]		 187.6(SOL)       287.6 (EOL)
    Mass in air [kg/m]		        47.68(SOL)       97.13 (EOL)
    Weight in sea water [N/m]	        439.4(SOL)        NA (EOL)

    Buoy property
    Mass of one buoy	Mb [kg]	        746.56(SOL)      704.30(EOL)
    Net Buoyancy of 1 module	[kg]	1000.0(SOL)      1050(EOL)
    Buoy outer diameter	Db [mm]	        1250.00(SOL)     1250.00(EOL)


The base model **LW_800mm_ESOL.yml** for test run can be accessed by using the following path,

.. code-block:: bash

   cd NEV\Floating Offshore Wind\05 Software\CABLEX\CodeSource

2. **MODEL ITERATION**: Download the **pc_conf_LS1.py**, make sure the python file and base model are in the same 
folder, open the VS terminal to the exact file path where above two files locates. Achieve case iteration/multiply work 
for Nominal Position with SOL/EOL Properties.

.. code-block:: bash

    python pc_conf_LS1.py


The case will be generated automatically with screen showing what the case generating now with layback showing. The scripts will be ending with the infomation 
for all generated cases, for **Length Failed** case, refers to the total length is smaller than the minimum line length at given laybacks while 
**Buoy_L Failed** ones referst to the buoy length is large than 2/3 of the total length which is not acceptable for Power Cable Design. Those information will
also be saved into data.txt file, For Example

::

    End of the batch
    Total number of models created:  4664
    Total number of Length Failed models:  2182
    Total number of Buoy_L Failed models:  294
    Time :  2024-02-05 11:39:28.744989
    Elapsed time : 579.515625 0.421875
    Total elapsed time: 579.09375 [s]

You now got all the simulation files with **DS1 & LS1** 

3. **SIMULTAIONS & POST PROCESSING**: download the **post_calculation_CABLEX_LW.py** from the aforementioned path, copy the file to the same directory where the case file generated.
Open **Orcaflex** batch processing reload all the case file and simulate the case, the post-processing results will be automatically shown as soon as the static simulation is finalised.

Run **dataSum_static.py** to summarise all the data file used for visualisation in CABLEX UI, you will get two seperate files with all data,

::

    Nominal_SOL_LS1.txt
    Nominal_EOL_LS1.txt


4. **VISUALISATION**: Transfer the results file from LS1 to the **CABLEX.exe** located directory, ususally the data is saved under the following path for the show case

.. code-block:: bash
    cd ./Pentlandstatics

double click **CABLEX.exe**, you will be able to see the knowledge and data base based on the LS1 site conditions

5. **SPECIFY PASS CASE**: Click **export pass case** button at CABLEX UI and saved it to the directory for LS2 simulations, make sure the file name is **allpass.txt**, 
a screenshot of the pass cases is shown as follows,

.. image:: _static/passcaseLS1.jpg
   :alt: passcaseLS1
   :width: 280px
   :height: 240px
   :align: center



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