# Related Work

## Standards

[ASAM OpenDrive](https://www.asam.net/standards/detail/opendrive/):
Road networks are specified in the OpenDrive format.
It is used to test simulation models in a co-simulation directly in the GitHub CI pipeline.

[ASAM OpenScenario](https://www.asam.net/standards/detail/openscenario/):
How objects move in a scene is described in the OpenScenario format.
It is used to test simulation models in a co-simulation directly in the GitHub CI pipeline.

[ASAM OpenSimulationInterface](https://github.com/OpenSimulationInterface/open-simulation-interface):
All simulation models on OpenMSL use OSI as the standard interface for model input and model output.

[Modelica FMI](https://fmi-standard.org/):
All models on OpenMSL are packaged as an FMU, compliant with the FMI standard.
This enables co-simulation of multiple models from different suppliers.

[SSP Traceability](https://github.com/PMSFIT/SSPTraceability):
To specify a system for co-simulation, the SSP standard is used.
This XML standard defines, which FMUs belong to a certain system and how they are connected in a so-called System Structure Definition (SSD).
Also, parameters can be assigned to the different FMUs.

## Other Projects

[esmini](https://github.com/esmini/esmini):
For co-simulation of OpenMSL models directly in the GitHub CI pipeline, esmini is used to play OpenScenario files as input for the models.

[FMPy](https://github.com/CATIA-Systems/FMPy):
To check, if an FMU build by the GitHub pipeline is conforming to the FMI standard, FMPy validate is used.

[FMU Compliance Checker](https://github.com/modelica-tools/FMUComplianceChecker):
Alongside the aforementioned FMPy, the official FMU Compliance Checker by Modelica is also used to ensure that all FMUs comply with the FMI standard.

[OpenMCx](https://github.com/eclipse/openmcx):
Simulations with multiple models packaged as FMUs need a co-simulation master.
To test models in the GitHub CI pipeline, OpenMCx is used to connect multiple FMUs according to a System Structure Definition (SSD).

[OSI Sensor Model Packaging](https://github.com/OpenSimulationInterface/osi-sensor-model-packaging):
OSMP is used as a template to package all models using OSI and FMI.
