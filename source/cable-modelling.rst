Modelling Iterations
====================

In the CABLEX workflow, model iterations play a crucial role in refining the power cable configuration through systematic adjustments. This section details the iterative process, starting from the established base model.
Utilising the parameters set in the Design Space, multiple cases are generated from the base model. Each case represents a unique configuration variation. This process involves systematic adjustments to the DS parameters and the generation of corresponding cases.


Base Model Refinement
---------------------

The base model, established in the Case Generation phase, serves as the foundation for model iterations. Before diving into iterations, ensure that the base model accurately represents the initial configuration based on client specifications and site data.

Design Parameters
-----------------

The Design Space from LS1-LS3 introduces parameters that govern the variations in the power cable configuration. These parameters are adjusted systematically to explore different possibilities. For a Lazy Wave Shape, five parameters are typically introduced:

::

    1. LayBack Length
    2. Total Length
    3. Buoy Uplift
    4. Buoy Centre to Centre
    5. 1st Buoy to clamp Distance

There will be four DS parameters since LS4 which make a lazywave shape power cable to either
a reverse plaint wave or plaint wave configuraiton power cables with the integration of tether 
and clamp, the related parameters goes as follows

::

    1. Tether Anchor
    2. Tether Length
    3. TDP Section Anchor
    4. TDP Section Length

However, since LS4, one or few Lazywave configuraiton will be applied with the  
aforementioned 4 DS parameters with tether and clamp and make it a full loop, which is 
more close to the real power cable modelling. 

The scripts can be accessed by to do the case multiple generation work

.. code-block:: bash

   cd UK-FDT-Tools\PowerCable\CABLEX\CaseGen





