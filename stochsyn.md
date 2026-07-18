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
STOCHASTIC SYNAPSE implements the modelling framework described in Savtchenko &amp; Rusakov, *"Glutamate&ndash;transporter unbinding in a probabilistic synaptic environment facilitates activation of distant NMDA receptors"* (Cells, 2023). It reproduces how the stochastic tissue geometry and transporter unbinding shape the reach of glutamate and the activation of distant receptors.

#### Downloads
Two ready-to-run implementations are provided:

- **Python package** (with graphical interface): [Python.zip]({{ '/assets/Python.zip' | relative_url }})
- **MATLAB version**: [MatLab.zip]({{ '/assets/MatLab.zip' | relative_url }})

#### Documentation and Support
For guidance and questions, please consult our [Support Page]({% link support.md %}) and join the discussion on the [Neuroalgebra Forum](https://forum.neuroalgebra.net/).
