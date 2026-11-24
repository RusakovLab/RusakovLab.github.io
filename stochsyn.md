---
layout: page
---
# STOCHASTIC SYNAPSE

#### Introducing STOCHASTIC SYNAPSE, a computational platform for exploring neurotransmitter diffusion and receptor activation in the crowded, probabilistic environment of the brain extracellular space.

**STOCHASTIC SYNAPSE** simulates the release, Brownian diffusion, and uptake of neurotransmitter molecules among realistic nanoscopic obstacles, and computes the resulting activation of synaptic and extrasynaptic receptors. It captures how the stochastic geometry of the neuropil and glutamate&ndash;transporter interactions shape signalling at and beyond the synaptic cleft, on the scale from nanometers to microns.

<div class="stochsyn-gallery">
  <img src="{{ '/assets/StochSyn1.png' | relative_url }}" alt="Stochastic Synapse simulation 1">
  <img src="{{ '/assets/StochSyn2.png' | relative_url }}" alt="Stochastic Synapse simulation 2">
  <img src="{{ '/assets/StochSyn3.png' | relative_url }}" alt="Stochastic Synapse simulation 3">
  <img src="{{ '/assets/StochSyn4.png' | relative_url }}" alt="Stochastic Synapse simulation 4">
</div>

#### Key Features
- **Monte Carlo diffusion**: tracks thousands of individual neurotransmitter molecules undergoing Brownian motion in a three-dimensional extracellular space.
- **Realistic stochastic environment**: neuronal and astroglial processes are represented as overlapping nanoscopic obstacles, with a tunable extracellular volume fraction and astroglial coverage.
- **Stochastic transporter kinetics**: glutamate binding, unbinding, and uptake by astroglial transporters are modelled probabilistically, including glutamate&ndash;transporter unbinding.
- **Receptor activation maps**: computes spatial and temporal maps of neurotransmitter concentration and of AMPA and NMDA receptor activation as a function of distance and time.
- **Interactive exploration**: a graphical interface lets you set parameters, run the diffusion, and view concentration and receptor-activation figures in one window.

#### Background
STOCHASTIC SYNAPSE implements the modelling framework developed in a series of studies by Savtchenko, Rusakov and colleagues (see Publications below). Together these works show how the stochastically shaped tissue geometry, glutamate buffering and uptake by astroglial transporters, and glutamate&ndash;transporter unbinding jointly shape the escape of neurotransmitter and the activation of synaptic and distant extrasynaptic receptors.

#### Publications
The STOCHASTIC SYNAPSE framework is based on the following studies, most recent first:

- Savtchenko LP, Rusakov DA. [Glutamate&ndash;transporter unbinding in probabilistic synaptic environment facilitates activation of distant NMDA receptors](https://pubmed.ncbi.nlm.nih.gov/37371080/). *Cells* **12** (12), 1610 (2023).
- Savtchenko LP, Rusakov DA. [Increased extrasynaptic glutamate escape in stochastically shaped probabilistic synaptic environment](https://pubmed.ncbi.nlm.nih.gov/36289667/). *Biomedicines* **10** (10), 2406 (2022).
- Savtchenko LP, Zheng K, Rusakov DA. [Buffering by transporters can spare geometric hindrance in controlling glutamate escape](https://pubmed.ncbi.nlm.nih.gov/34366791/). *Frontiers in Cellular Neuroscience* **15**, 707813 (2021).
- Savtchenko LP, Zheng K, Rusakov DA. [Conductance of porous media depends on external electric fields](https://pubmed.ncbi.nlm.nih.gov/33609495/). *Biophysical Journal* **120** (8), 1431&ndash;1442 (2021).
- Vergnano AM, Rebola N, Savtchenko LP, Pinheiro PS, Casado M, Kieffer BL, Rusakov DA, Mulle C, Paoletti P. [Zinc dynamics and action at excitatory synapses](https://pubmed.ncbi.nlm.nih.gov/24908489/). *Neuron* **82** (5), 1101&ndash;1114 (2014).
- Savtchenko LP, Rusakov DA. [Moderate AMPA receptor clustering on the nanoscale can efficiently potentiate synaptic current](https://pubmed.ncbi.nlm.nih.gov/24298165/). *Philosophical Transactions of the Royal Society B* **369** (1633), 20130167 (2014).
- Sylantyev S, Jensen TP, Ross RA, Rusakov DA. [Cannabinoid- and lysophosphatidylinositol-sensitive receptor GPR55 boosts neurotransmitter release at central synapses](https://pubmed.ncbi.nlm.nih.gov/23472002/). *Proceedings of the National Academy of Sciences USA* **110** (13), 5193&ndash;5198 (2013).
- Savtchenko LP, Sylantyev S, Rusakov DA. [Central synapses release a resource-efficient amount of glutamate](https://pubmed.ncbi.nlm.nih.gov/23242311/). *Nature Neuroscience* **16** (1), 10&ndash;12 (2013).
- Sylantyev S, Savtchenko LP, Niu YP, Ivanov AI, Jensen TP, Kullmann DM, Xiao MY, Rusakov DA. [Electric fields due to synaptic currents sharpen excitatory transmission](https://pubmed.ncbi.nlm.nih.gov/18369150/). *Science* **319** (5871), 1845&ndash;1849 (2008).
- Savtchenko LP, Rusakov DA. [The optimal height of the synaptic cleft](https://pubmed.ncbi.nlm.nih.gov/17261811/). *Proceedings of the National Academy of Sciences USA* **104** (6), 1823&ndash;1828 (2007).

#### Downloads
A ready-to-run implementation is provided:

- **Python package** (with graphical interface): [Python.zip]({{ '/assets/Python.zip' | relative_url }})
{% comment %}
Temporarily hidden; restore by moving the line below out of this comment block
and changing the sentence above back to "Two ready-to-run implementations are provided:".
The file assets/MatLab.zip is still in the repository.
- **MATLAB version**: [MatLab.zip]({{ '/assets/MatLab.zip' | relative_url }})
{% endcomment %}

#### Documentation and Support
For guidance and questions, please consult our [Support Page]({% link support.md %}) and join the discussion on the [Neuroalgebra Forum](https://forum.neuroalgebra.net/).
