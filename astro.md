---
layout: page
---
# ASTRO
<!--
<div style="width: 50%; float: left; margin-right: 5px;"><img src="assets/astro.jpg" alt="Astro"></div>
-->
<img src="{% link assets/astro.jpg %}" alt="" loading="lazy">

**ASTRO** is a computational tool to construct a realistic multi-compartmental astrocyte 
model that can be biophysically interrogated in [NEURON](https://www.neuron.yale.edu/neuron/)
computational environment, on the scale from nanometers to the entire cell morphology. **ASTRO** generates stochastically cell nanoscopic protrusions based on their real-world parameters and enables dynamic interactions between the modelled astrocyte and the surrounding 3D tissue environment.

#### Installation

**There are three available installations of ASTRO**
1. Basic source code. Local and remote computation on your own computer.
2. Self-installing version. Local computation. The version is available after registration.
3. Self-installing version. Local and Amazon clouds computations. Users ONLY pay 
   for the time use of Amazon AWS cloud resources.


#### Installing ASTRO

1. **"Web Astro"** - The installation version, with a computational multiprocessor 
core, easily switch from the local computer to the remote Amazon cloud, can be downloaded
from the site after registration.<br>System Requirements for Amazon Web installation of **ASTRO**:
    - OS : Windows 7/10/11.
    - Fast internet connections.
    - PuTTY agent installation: PuTTY download
    - SSH key can be downloaded after registration.
    - Astro-archive version is available after registration. 

2. **"Basic Astro"** - The source code of installation can be downloaded from [ZIP file ASTRO]({% link assets/Astro-master.zip %})
<br>System Requirements for basic installation of **ASTRO**:
    - OS : Linux (Remote cluster) and Windows 7/10/11 (Host computer).
    - The computer languages : C++, MATLAB not older than 2013 and Neuron 7.0.
    - Type of operation : Sequential and parallel (MPI) computing.
    - Fast internet connections.
    - Basic version of Astro can be downloaded from [ZIP file ASTRO]({% link assets/Astro-master.zip %}).

3. **Most ASTRO functions have been superseded by BRAINCELL.**

#### Documentation
Manual and API documentation can be found in [User Guide PDF]({% link assets/ASTRO_User_Guide_v7.pdf %}). 


