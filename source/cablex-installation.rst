Installation
============

To get started with using CABLEX, you have to be aware of the file structure of CABLEX and
where to store you simulation data inside for pre/post-processing or visualsation.

File Structure
--------------

There are only two folders included in the software, i.e., bmp & data, where :file:`bmp` is usually to install all
necessary dependencies and documentation while :file:`data` usually save the simulation results after post-processing scripts. 
All data files are named with :file:`Offsets_MarineGrowth_LoadingSpace_Cable_Buoy.txt`

Offsets
~~~~~~~
The Offsets usually includes the following four scenarios which usually represents the offsets flexible during their real-life scenarios
For the :file:`Norminal` One, it is applicable for both static and dynamic results, while the :file:`Near Far Cross` usually only appear 
in the static analysis (LS1-LS3)

.. code-block:: text
    :linenos:
    Nominal
    Far
    Near
    Cross

Marine Growth
~~~~~~~~~~~~~
Marine growth refers to the accumulation of marine organisms on underwater structures, impacting submerged surfaces in aquatic environments, 
which can alter the performance of flexible materials over time. In this case, :file:`SOL` and :file:`EOL` which represents scenarios under
start of life and end of life.

.. code-block:: text
    :linenos:
    SOL
    EOL

Loading Space
~~~~~~~~~~~~~
Loading Space refers as follows:

LS1: rough static check with wide range of Layback/TotalLength/Buoy  
LS2: detailed static check with offsets based on finer configurations obtained from the pass cases(not taut and SAG/HOG not touching SB/SWL) from LS1 
LS3: more detailed static check with offsets & current based on the pass cases from LS2 (SAG/HOG clearance 15% water depth) 
LS4: tether and clamp added with external checks to pass the entire config to dynamic analysis
LS5: general dynamic check with specified time domain series for powercable fairleadpoint at ESS (50-y return period) 
LS6: fatigue analysis with cyclic runs 


+---------------------+---------------------------+
|         LS          |         Content           |
+=====================+===========================+
|   Loading Space 1   |     LW Static Nominal     |
+---------------------+---------------------------+
|   Loading Space 2   |     LW Static Offsets     |
+---------------------+---------------------------+
|   Loading Space 3   | LW Static Offsets & Cur   |
+---------------------+---------------------------+
|   Loading Space 4   |   PW/RPW Static Add       |
+---------------------+---------------------------+
|   Loading Space 5   |  PW/RPW Dynamic ESS & Dir |
+---------------------+---------------------------+
|   Loading Space 6   |      PW/RPW Fatigue       |
+---------------------+---------------------------+

Canble/Buoy
~~~~~~~~~~~
Cable and Buoy usually represents which specified cable/buoy or even tether/clamp model is utlised in the simulations,
for example, :file:`300mm Al` or :file:`800mm Cu` 

Installation
------------

For Running the code, double click "CABLEX.exe", it may take 60s for the User Interface to open.