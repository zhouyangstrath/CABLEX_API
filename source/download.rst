Downloads
=========

To get started with CABLEX, you can download the latest version using the following two ways:

Software Downloads
------------------

The code is compiled to the executables after each release to aid engineers optimising the DIAC Configuration. Those compiled exe files 
can be downloaded via:

.. code-block:: bash
   cd L:\18 NEV\Floating Offshore Wind\05 Software\CABLEX


Using Git
---------

Make sure you have been added to the moderators at UK-FDT-Tools Groupds in DevOps, if not, contact Moderators for help,
it is always able to access the source code of CABLEX, to clone the repository, run the following command in your terminal:

.. code-block:: bash

   git clone https://Subsea-Dynamic-Analysis@dev.azure.com/Subsea-Dynamic-Analysis/UK-FDT-Tools/_git/UK-FDT-Tools


Once you have cloned the repository, navigate to the project directory:

.. code-block:: bash

   cd UK-FDT-Tools/PowerCable/CABLEX

System Requirements
-------------------

This software is built on Python, and thus, the system should meet the following hardware and software requirements:

- **Operating System:** Recommended for Windows 10 or 11.
- **Memory (RAM):** At least 16 GB.
- **CPUs (cores):** At least 16 cores(SIM) & 8 cores(UI)
- **Storage Space:** At least 200 MB available space.

**Python Environment:**

Ensure that Python is installed on your system. It is recommended to use Python 3.x.

.. code-block:: bash

   python --version

If not installed, download and install Python from the (https://www.python.org/).

**Dependency Installation:**

Install the required dependencies in the Python environment. Execute the following command in the terminal or command prompt:

.. code-block:: bash

   pip install -r requirements.txt


Now, it is ready to use CABLEX with generic version with full code access.

