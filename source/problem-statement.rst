Problem Statement
=================

To examine the best cable configuration from a given clinets specifications, or the knowledgebase under the provided sites
metocean data. The work flow of CABLEX is shown as follows, which is initiated from Client/TFMC inputs and returns with an optimized configuration.

Analysis Process
----------------

Typically, seven stages are presented to assist us in achieving a better configuration. It begins with documentation of client/TFMC engineers' specifications, 
On the client side, including site conditions, RNA and floater geometries, gross properties, metocean data, and client specifications. TFMC engineers will 
also be provided with information on buoy, cable, clamp, bend stiffener types, along with installation cost requirements.


.. image:: _static/workflow.png
   :alt: workflow
   :width: 700px
   :height: 233px
   :align: center


The following figure presents a simplified Lazy Wave Shape Power Cable from (LS1-LS3). 
It is typically considered in the initial stages to establish an optimized configuration, 
laying a solid foundation for subsequent modeling and optimization. The current methodology introduces the concept 
of the **Design Space** or **DS**, which is represented by several parameters. For a Lazy Wave Shape, five parameters are introduced, as shown below:

::

    Power Cable Configuration:
                
    Fairlead
    |\         Hog
    | \        /~\~ Buoy
    |  \      /~  \~
    |   \    /~    \~   TotalLength(PC)
    |    \  /       \
    |     \/         \
    |    Sag          \  Hang-off  
    |________________________________ 
    LayBack      


::

    LayBack: LayBack
    Total Length: LW Power Cable Total Length
    Buoy:  Buoy Uplift Force
    Buoy_CC:  Buoy to Buoy Center to Centre Distance
    1st Buoy: Clamp/Hang-off position to 1st Buoy Distance


Methodology
-----------
.. image:: _static/workflow2.png
   :alt: workflow
   :width: 750px
   :height: 565px
   :align: center

Figure present the methodology of CABLEX