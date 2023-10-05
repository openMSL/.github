# ENVITED Open Source Model & Simulation Library

> *"OpenMSL is a central hub demonstrating the interaction between models, standards and tools from the vast space of ADAS simulation condensing years of research in a single organization." - Dr. Clemens Linnhoff, CTO at Persival GmbH*

![tp header](/doc/img/envited.png)

[![Header Image](https://img.shields.io/twitter/follow/ASCS_eV?label=Follow&style=social)](https://twitter.com/ASCS_eV)

ENVITED stands for **Environment for Virtual Test Drive** encompassing all components for virtual test and validation of Advanced Driver Assistent Systems (ADAS)
including but not limited to standardized data sets, e.g. digital maps, scenario data, simulation models and their respective test and validation methods.
OpenMSL aims to connect and demonstrate the seemless interaction of projects in the domain using elaborate test pipelines, also to assure the compliance of all simulation entities with relevant standards.
A list of utilized standards and tools can be found [here](/doc/related_work.md).

All repositories are organized in sub-libraries and each sub-library (SL) represents the best practices in the automotive industry on
how to use, create and apply standard compliant simulation data and models regarding a specific topic or application area guided by expert maintainers of the ENVITED community.

As part of these best practices, OpenMSL provides unified test architectures for simulation components.
For OSMP compliant simulation models, an [OSMP Test Architecture](/doc/osmp_test_architecture.md) is definied.
The architecture is applied in the template repositories of the corresponding sub-libraries.

Learn more about the ENVITED research cluster of the Automotive Solution Center for Simulation e.V, our governance rules, contribution guidelines and our code of conduct [here](/README.md).

We are looking forward to welcome you as member of our community!

## OpenMSL Sub-Libraries

- [SL1 - Perception Sensor Models](#sl1---perception-sensor-models)
  - [sl-1-0-sensor-model-repository-template](#sl-1-0-sensor-model-repository-template)
  - [sl-1-1-reflection-based-radar-object-model](#sl-1-1-reflection-based-radar-object-model)
  - [sl-1-2-reflection-based-lidar-object-model](#sl-1-2-reflection-based-lidar-object-model)
  - [sl-1-3-object-based-generic-perception-object-model](#sl-1-3-object-based-generic-perception-object-model)
  - [sl-1-4-object-based-camera-object-model](#sl-1-4-object-based-camera-object-model)

- [SL2 - Traffic Participant Models](#sl2---traffic-participant-models)
  - [sl-2-0-traffic-participant-model-repository-template](#sl-2-0-traffic-participant-model-repository-template)

- [SL3 - Scenario Data](#sl3---scenario-data)
  - [sl-3-1-osc-alks-scenarios](#sl-3-1-osc-alks-scenarios)

- [SL4 - Static Environment Data](#sl4---static-environment-data)

- [SL5 - Tooling](#sl5---tooling)
  - [sl-5-1-srmd-validator](#sl-5-1-srmd-validator)
  - [sl-5-2-osi-field-checker](#sl-5-2-osi-field-checker)
  - [sl-5-3-osmp-network-proxy](#sl-5-3-osmp-network-proxy)
  - [sl-5-4-standalone-osi-trace-file-player](#sl-5-4-standalone-osi-trace-file-player)
  - [sl-5-5-osi-trace-file-player](#sl-5-5-osi-trace-file-player)
  - [sl-5-6-osi-trace-file-writer](#sl-5-6-osi-trace-file-writer)

---

## SL1 - Perception Sensor Models

> This sub-library is a collection of [OSI](https://github.com/OpenSimulationInterface/open-simulation-interface) compliant sensor models according to the [OSMP](https://github.com/OpenSimulationInterface/osi-sensor-model-packaging) specification including a template repository
demonstrating the [Credible Simulation Process](https://setlevel.de/assets/forschungsergebnisse/Credible-Simulation-Process-v1.0.pdf) by running full scale [SSP](https://ssp-standard.org/) based co-simulations in the CI pipeline.

Initiated: 2022-07-25

### Maintainer

  [![avatar](../doc/img/avatar/LukasElster.png) Lukas Elster](https://github.com/LukasElster) (FZD TU Darmstadt)

  [![avatar](../doc/img/avatar/ClemensLinnhoff.png) Clemens Linnhoff](https://github.com/ClemensLinnhoff) (Persival GmbH)

  [![avatar](../doc/img/avatar/JuergenWille.png) Jürgen Wille](https://github.com/FM-juergenW) (FrontMod GmbH)

### Repositories

#### sl-1-0-sensor-model-repository-template

  > Enter a short description of the model.
  > What is the purpose of the model?
  > What is the general modeling approach?
  > What inputs does the model need and what outputs does it generate?
  >
  > more info: [click here](https://github.com/openMSL/sl-1-0-sensor-model-repository-template)

#### sl-1-1-reflection-based-radar-object-model

  > This model is a Reflection Based Radar Model based on the [Modular OSMP Framework](https://gitlab.com/tuda-fzd/perception-sensor-modeling/modular-osmp-framework) by FZD.
  > It is a highly parameterizable sensor system model including detection calculation and object tracking simulation.
  > The model received radar reflection data calculated in a simulation tool beforehand e.g. with ray tracing.
  > The model outputs are radar detections and detected moving objects.
  >
  > more info: [click here](https://github.com/openMSL/sl-1-1-reflection-based-radar-object-model)

#### sl-1-2-reflection-based-lidar-object-model

  > The current version of the model is build on the enhancements to the Open Simulation Interface from the publicly funded SETLevel project.
  > It is therefore dependent on the non-standard [SL OSI](https://gitlab.setlevel.de/open/osi) and not [ASAM OSI](https://github.com/OpenSimulationInterface/open-simulation-interface).
  >
  > This is the FZD Reflection Based Lidar Model based on the FZD OSI Sensor Model Packaging Framework.
  > It is a highly parameterizable sensor system model including detection calculation and object tracking simulation.
  > The model gets lidar reflection calculated in a simulation tool beforehand e.g. with ray tracing.
  > The model outputs are lidar detections and detected moving objects.<br>
  >
  > more info: [click here](https://github.com/openMSL/sl-1-2-reflection-based-lidar-object-model)

#### sl-1-3-object-based-generic-perception-object-model

  > This model is a highly parameterizable generic perception sensor and tracking model. It can be parameterized as a Lidar or a Radar. The model is based on object lists and all modeling is performed on object level.
  > It includes typical sensor artifacts like soft FoV transitions, different detection ranges for different targets occlusion effects depending on the sensor technology as well as simulation of tracking behavior.
  > The model output are object lists for OSI SenorData moving objects.
  >
  > The architecture of the model as well as the parameterization structure are designed to be as generic as possible
  > to fit both radar and lidar sensors to utilize similarities in signal propagation and signal processing in both technologies.
  > This way, the model can be parameterized to model different kinds of lidar and radar sensors. To give an example: You can set an irradiation pattern for the modeled sensor. Depending on the sensor technology this can either be an antenna gain pattern for radar or a beam pattern for lidar.
  >
  > more info: [click here](https://github.com/openMSL/sl-1-3-object-based-generic-perception-object-model)

#### sl-1-4-object-based-camera-object-model

  > This model is a parameterizable object based video perception sensor and tracking model using the interface OSI.   The model was developed in the project SetLevel by Bosch. The model should simulate some basic video typical effects in a phenomenological way.
  > The "object based camera object model" is based on object lists and all modeling is performed on object level. The model output are object lists for OSI SenorData moving and stationary objects.
  >
  > The outer layer of the model is the OSI Sensor Model Packaging (OSMP). It specifies ways in which models  using the Open Simulation Interface (OSI) are to be packaged for their use in simulation environments using FMI 2.0.
  > For more detailed information see the official documentation.
  >
  > more info: [click here](https://github.com/openMSL/sl-1-4-object-based-camera-object-model)

---

## SL2 - Traffic Participant Models

This sub-library is a set of OSI compliant traffic participant models, which include pedestrian models, SSP based ALKS systems, automated road users and others to demonstrate closed loop simulations in combination with other sub-libraries utilizing open-source simulators such as [esmini](https://github.com/esmini/esmini).

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

### Maintainer

- TBD
- TBD
- TBD

### Repositories

#### sl-2-0-traffic-participant-model-repository-template

  > Under development
  >
  > more info: [click here](https://github.com/openMSL/sl-2-0-traffic-participant-model-repository-template)

---

## SL3 - Scenario Data

This sub-library contains example scenario data following the [ASAM OpenSCENARIO](https://www.asam.net/standards/detail/openscenario/) standard to provide interpretations for legislative documents such as the UN Regulation No. 157 in order to discuss them in the community.
In addition, the best practices to establish quality gates for scenario databases to clearly show the quality of scenario data are shown.

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

### Maintainer

- TBD (BMW AG)
- TBD
- TBD

### Repositories

#### sl-3-1-osc-alks-scenarios

  > The here provided 15 concrete parametrized test scenarios are derived from the 6 subject areas analogous to Annex 5, Chapter 4.1-4.6 as an initial attempt to clarify the described set of functional scenarios.
  >
  > Each concrete scenario is complemented by a variation file to form a logical scenario, which then represents a set of concrete scenarios.
  > By applying the parameter variation defined in the variation files to the parameters in the concrete scenarios, multiple concrete scenarios can be derived or generated to cover the required scenario space.
  >
  > The focus of the here provided scenarios is on securing the planning aspects of an "Automated Lane Keeping System".
  > By extending the scenarios with environmental conditions (e.g. light, rain or wind) or references to e.g. 3D models, aspects of sensor and actuator technology could also be simulated and validated.
  >
  > more info: [click here](https://github.com/asam-oss/OSC-ALKS-scenarios)

---

## SL4 - Static Environment Data

The German research project [GaiaX 4 PLC-AAD](https://www.gaia-x4plcaad.info/) develops quality metrics and tools to evaluate the successful integration of [ASAM OpenDRIVE](https://www.asam.net/standards/detail/opendrive) maps
with e.g. [glTF](https://www.khronos.org/gltf/) 3D models and their respective material data extentions.

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

### Maintainer

- TBD (BMW AG)
- TBD
- TBD

### Repositories

- In discussion

---

## SL5 - Tooling

This sub-library contains various tools to import, export, analyze and visualize co-simulation data.

Initiated: Call for participation. Get engaged [hello@envited.market](mailto:hello@envited.market)

### Maintainer

- TBD (Persival GmbH)
- TBD
- TBD

### Repositories

#### sl-5-1-srmd-validator

  > This python code is meant to be used in a CI pipeline, e.g. a GitHub Action. It looks for SRMD files in the root directory of a repository, this repo is cloned into. The found SRMD files are validated against the SRMD schema from [SSPTraceability](https://github.com/PMSFIT/SSPTraceability/).
  >
  >more info: [click here](https://github.com/openMSL/sl-5-1-srmd-validator)

#### sl-5-2-osi-field-checker

  > This FMU checks if fields are missing in a received SensorData. It is meant to be used in a co-simulation connected to the output of the model under test. It will output missing osi fields in the format of GitHub annotations, so that it can be used directly in a GitHub CI pipeline.
  > The image below shows an example of a failed pipeline due to missing OSI fields in the SensorData.
  >
  >more info: [click here](https://github.com/openMSL/sl-5-2-osi-field-checker)

#### sl-5-3-osmp-network-proxy

  > This Network Proxy FMU can receive SensorView and SensorData via TCP/IP using ZeroMQ. The received data is directly given to the FMU output. The proxy can also send SensorView oder SensorData received as FMU input via TCP/IP to a given IP address and port.
  >
  > more info: [click here](https://github.com/openMSL/sl-5-3-osmp-network-proxy)

#### sl-5-4-standalone-osi-trace-file-player

  > This mini application can read a binary ASAM OSI trace file (SensorData or SensorView) and send it step by step via TCP using ZeroMQ.
  >
  > more info: [click here](https://github.com/openMSL/sl-5-4-standalone-osi-trace-file-player)

#### sl-5-5-osi-trace-file-player

  > This [FMU](https://fmi-standard.org/) is able to play binary OSI trace files. The folder containing the trace files has to be passed as FMI parameter *trace_path*.
  > The trace file player is build according to the [ASAM Open simulation Interface (OSI)](https://github.com/OpenSimulationInterface/open-simulation-interface) and the [OSI Sensor Model Packaging (OSMP)](https://github.com/OpenSimulationInterface/osi-sensor-model-packaging) examples.
  >
  > more info: [click here](https://github.com/openMSL/sl-5-5-osi-trace-file-player)

#### sl-5-6-osi-trace-file-writer

  > This [FMU](https://fmi-standard.org/) is able to write binary OSI SensorData trace files. The folder the trace files shall be written to has to be passed as FMI parameter *trace_path*.
  > The trace file writer is build according to the [ASAM Open simulation Interface (OSI)](https://github.com/OpenSimulationInterface/open-simulation-interface) and the [OSI Sensor Model Packaging (OSMP)](https://github.com/OpenSimulationInterface/osi-sensor-model-packaging) examples.
  >
  > more info: [click here](https://github.com/openMSL/sl-5-6-osi-trace-file-writer)
