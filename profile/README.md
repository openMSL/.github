# ENVITED Open Source Model & Simulation Library

> *"OpenMSL is a central hub demonstrating the interaction between models, standards and tools from the vast space of ADAS simulation condensing years of research in a single organization." - Clemens Linnhoff, CTO at Persival GmbH*

![tp header](/doc/img/envited.png)

[![Header Image](https://img.shields.io/twitter/follow/ASCS_eV?label=Follow&style=social)](https://twitter.com/ASCS_eV)

ENVITED stands for **Environment for Virtual Test Drive** encompassing all components for virtual test and validation of Advanced Driver Assistent Systems (ADAS)
including but not limited to standardized data sets like e.g. digital maps, scenario data, simulation models and their respective test and validation methods.
OpenMSL aims to connect and demonstrate the seemless interaction of projects in the domain using elaborate test pipelines, also to assure the compliance of all simulation entities with relevant standards.
A list of utilized standards and tools can be found [here](/doc/related_work.md).

All repositories are organized in sub libraries and each sub library (SL) represents the best practices in the automotive industry on
how to use, create and apply standard compliant simulation data and models regarding a specific topic or application area guided by expert maintainers of the ENVITED community.

Learn more about the ENVITED research cluster of the Automotive Solution Center for Simulation e.V, our governance rules, contribution guidelines and our code of conduct [here](/README.md).

We are looking forward to welcome you as member of our community!

## Sub Libraries

### SL1 - Perception Sensor Models

A collection of [OSI](https://github.com/OpenSimulationInterface/open-simulation-interface) compliant sensor models according to the [OSMP](https://github.com/OpenSimulationInterface/osi-sensor-model-packaging) specification including a template repository 
demonstrating the [Credible Simulation Process](https://setlevel.de/assets/forschungsergebnisse/Credible-Simulation-Process-v1.0.pdf) by running full scale [SSP](https://ssp-standard.org/) based co-simulations in the build pipeline.

Initiated: 2022-07-25
  
#### Maintainer

- [Lukas Elster](https://github.com/LukasElster) (FZD TU Darmstadt)
- [Clemens Linnhoff](https://github.com/ClemensLinnhoff) (Persival GmbH)
- [Jürgen Wille](https://github.com/FM-juergenW) (FrontMod GmbH)
  
#### Repositories

- [sl-1-0-sensor-model-repository-template](https://github.com/openMSL/sl-1-0-sensor-model-repository-template)
- [sl-1-1-reflection-based-radar-object-model](https://github.com/openMSL/sl-1-1-reflection-based-radar-object-model)
- [sl-1-2-reflection-based-lidar-object-model](https://github.com/openMSL/sl-1-2-reflection-based-lidar-object-model)
- [sl-1-3-object-based-generic-perception-object-model](https://github.com/openMSL/sl-1-3-object-based-generic-perception-object-model)
- [sl-1-4-object-based-camera-object-model](https://github.com/openMSL/sl-1-4-object-based-camera-object-model)
- [sl-1-5-sensor-model-testing](https://github.com/openMSL/sl-1-5-sensor-model-testing)

### SL2 - Traffic Participant Models

A set of OSI compliant traffic participant models which include pedestrian models, SSP based ALKS systems, automated road users and others to demonstrate closed loop simulations in combination with other sub libraries utilizing open-source simulators like [esmini](https://github.com/esmini/esmini).

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

#### Maintainer

- TBD
- TBD
- TBD
  
#### Repositories

- [sl-2-0-traffic-participant-model-repository-template](https://github.com/openMSL/sl-2-0-traffic-participant-model-repository-template)

### SL3 - Scenario Data

Example scenario data following the [ASAM OpenSCENARIO](https://www.asam.net/standards/detail/openscenario/) standard to provide interpretations for legislative documents like the UN Regulation No. 157 in order to discuss them in the community.
In addition the best practices to establish quality gates for scenario databases to clearly show the quality of scenario data are to be shown.

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

#### Maintainer

- TBD (BMW AG)
- TBD
- TBD
  
#### Repositories

- [sl-3-1-osc-alks-scenarios](https://github.com/asam-oss/OSC-ALKS-scenarios)

### Static Environment Data

The German research project [GaiaX 4 PLC-AAD](https://www.gaia-x4plcaad.info/) develops quality metrics and tools to evaluate the successful integration of [ASAM OpenDRIVE](https://www.asam.net/standards/detail/opendrive) maps
with e.g. [glTF](https://www.khronos.org/gltf/) 3D models and their respective material data extentions.

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

#### Maintainer

- TBD (BMW AG)
- TBD
- TBD
  
#### SL4 - Repositories

- In discussion
- 