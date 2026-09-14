# PRECISION

**Physics-infoRmed machine lEarning of Cloud mIcrophySics for hIgh-resolution Earth system modeling with Observationally constrained oNline training**

| | |
| --- | --- |
| Lead institution | Argonne National Laboratory |
| Principal Investigator | Yan Feng |
| Program | U.S. Department of Energy Genesis Mission; selected in the first round of Genesis Mission research projects (DOE announcement of July 22, 2026; DE-FOA-0003612) |

## Scientific challenge

Precipitation and high-impact weather remain among the least well-predicted quantities in Earth system models (ESMs), and the representation of cloud microphysics is a leading source of that uncertainty. The processes that determine the onset, location, and intensity of precipitation, including droplet activation, condensational growth, and collision–coalescence, are coupled to turbulence at scales from micrometres to metres, whereas ESM grid cells span kilometres to tens of kilometres. Bulk microphysics parameterizations bridge this gap with prescribed particle size distributions and empirically tuned process rates, and the resulting errors propagate into simulated precipitation, cloud radiative effects, and extremes.

Direct numerical simulation (DNS) resolves the microphysics–turbulence interactions explicitly, but only in domains of order a metre and at a computational cost that precludes direct use in ESMs. Machine-learning parameterizations offer a route for transferring process-level fidelity to ESMs, but existing approaches have two recognized limitations: models trained offline on coarse-resolution data do not represent the underlying process physics, and models coupled to a host model after offline training are prone to instability and drift.

## Approach

PRECISION is a hybrid physics–machine-learning framework that connects process-resolving simulation, high-resolution atmospheric modeling, and observations through three stages of training:

1. **Physics-informed learning from DNS.** Neural networks representing cloud microphysical processes are trained on high-fidelity DNS in which microphysics and turbulence are explicitly resolved, with physical constraints imposed on the learned representation.
2. **Online training within a differentiable atmospheric model.** The networks are embedded in a GPU-accelerated, fully differentiable atmospheric model. Differentiability of the host model permits end-to-end training of the embedded networks within the coupled system, which addresses the stability limitations of offline-trained parameterizations while enabling efficient high-resolution simulation.
3. **Observational constraint.** Observations from the DOE Atmospheric Radiation Measurement (ARM) user facility and from satellite platforms are incorporated into the online training, so that the learned microphysics is continually constrained by the observed atmosphere.

The outcome is a representation of cloud microphysics that is anchored in resolved process physics, numerically stable within the host model, constrained by observations, and transferable to regional and global ESMs, with the objective of improving prediction of precipitation, storms, droughts, and floods on subseasonal to decadal timescales.

## Connection to the ARM user facility

ARM is a DOE Office of Science user facility managed by the Biological and Environmental Research (BER) program. Its mission is to provide the research community with strategically located atmospheric observatories that improve the understanding and representation of cloud, aerosol, and precipitation processes in Earth system models, in support of DOE's science, energy, and national security missions. ARM operates continuously instrumented fixed observatories in Oklahoma, Alaska, and the Eastern North Atlantic, together with mobile facilities deployed for targeted field campaigns, and its ground-based remote-sensing and in situ measurements of cloud and precipitation properties are among the most comprehensive long-term records available.

In PRECISION, ARM observations, together with satellite observations, provide the observational constraint in the third training stage, closing the loop between process-resolving simulation and the observed atmosphere. Using ARM data to constrain a microphysics representation destined for ESMs is the purpose for which the facility was established, and PRECISION extends that use from the evaluation of parameterizations to their training.

## Alignment with DOE priorities

- **Genesis Mission.** The Genesis Mission is DOE's national initiative, launched on November 24, 2025 and directed by the Under Secretary for Science, to unite the national laboratories, industry, and academia in harnessing AI for breakthroughs in energy dominance, discovery science, and national security. The first round of Genesis Mission research projects, in which PRECISION was selected, is intended to design and demonstrate research workflows that integrate AI with scientific investigation and to evaluate rigorously whether those approaches improve predictive capability. PRECISION's three-stage workflow, which couples AI models to process-resolving simulation, a differentiable host model, and a DOE user facility, is such a workflow.
- **Genesis Mission national challenges.** Precipitation prediction bears directly on the national challenge *Predicting U.S. Water for Energy*, which identifies water availability as essential to expanding the production and utilization of energy and to the nation's health and security. Argonne's Genesis Mission portfolio explicitly targets improved prediction of water availability and extreme weather and improved reliability of energy systems.
- **Office of Science, Biological and Environmental Research.** Improving the representation of cloud and precipitation processes in ESMs is a long-standing BER objective and the mission of the ARM user facility. The parameterization problem addressed by PRECISION is common to all ESMs, including DOE's Energy Exascale Earth System Model (E3SM).
- **Energy infrastructure and resilience.** Reliable prediction of precipitation, storms, droughts, and floods supports the planning and operation of energy infrastructure, water resource management, and emergency preparedness.

## Media

<a href="https://www.youtube.com/watch?v=aJEKj3ErOfc"><img src="https://img.youtube.com/vi/aJEKj3ErOfc/maxresdefault.jpg" width="480" alt="DOE's Genesis Mission: Improving Extreme Weather Predictions with AI"></a>

[DOE's Genesis Mission: Improving Extreme Weather Predictions with AI](https://www.youtube.com/watch?v=aJEKj3ErOfc), Argonne National Laboratory.

## References and links

- [PRECISION project page, Argonne National Laboratory](https://www.anl.gov/genesis-mission/projects/physics-Informed-machine-learning-of-cloud-microphysics-for-high-resolution-earth-system-modeling-with-observationally-constrained-online-training)
- [The Genesis Mission, U.S. Department of Energy](https://www.energy.gov/genesis-mission)
- [Genesis Mission National Science and Technology Challenges](https://www.energy.gov/undersecretaryforscience/genesis-mission/genesis-mission-national-science-and-technology-challenges)
- [First Genesis Mission projects selected for award negotiations, DE-FOA-0003612, list posted July 22, 2026](https://science.osti.gov/-/media/funding/pdf/Awards-Lists/2026/GM-RFA-Awards-List.pdf)
- [Argonne to lead AI research projects under the Department of Energy's Genesis Mission, July 22, 2026](https://www.anl.gov/article/argonne-to-lead-ai-research-projects-under-the-department-of-energys-genesis-mission)
- [Atmospheric Radiation Measurement (ARM) user facility](https://www.arm.gov)

## About this organization

This organization hosts source code and documentation developed for PRECISION.
