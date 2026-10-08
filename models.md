---
layout: page
title: MODELS
hide_title: true
order: 40
---

## Computational models created in-house 

### BRAINCELL (neuron and astrocyte) Models

- [Model 1: Basket Cell - GABA Dynamics]({% link models/basket.zip %})
- [Model 2: CA1 Pyramidal Neuron - Spiking Activity]({% link models/CA1PyramidalNeuron.zip %})
- [Model 3: CA1 Astrocyte - Calcium Waves]({% link models/CA1AstrocyteCaWaves.zip %})

To integrate custom mechanisms into BrainCell, follow these steps:

1. **Upload the ZIP Archive**: The archive should include:
   - A cell model with all mechanisms and geometry.
   - A DLL file specific to the mechanisms.
2. **Unpack the Archive**: Extract the contents of the ZIP archive into the `Nanogeometry` folder of BrainCell.
3. **Load the HOC File**: At the very beginning of activating the **BrainCell Export (BrainCell)** option, load the corresponding HOC file from the archive.


### ARACHNE (network) models

- [Model 1: GABA Waves in CA1 Interneuron Network]({% link models/GABAWave.zip %})
- [Model 2: Rippling Waves in Interneuron-Pyramidal Network]({% link models/ElectricalWaveInterPyramid.zip %})
- [Model 3: Stochastic Dynamics in Interneuron-Pyramidal Network]({% link models/InterPyramidcurrent.zip %})


To use ARACHNE, download and install the software first:  
[Download Arachne Installer for Windows]({% link assets/UCLAppInstaller_web.1.5.zip %})

**All uploaded files must be unzipped and placed in the following directory:**
`C:\Users\<username>\arachne\local\`
Replace `<username>` with your actual Windows username.


### ASTRO (astrocyte) Models

- [Model 1: Example Nanostructure - MATLAB File]({% link models/ExampleofNanostructure.fig %})
- [Model 2: Single Astrocyte Finger - MATLAB File]({% link models/SinglefNanostructure.fig %})
