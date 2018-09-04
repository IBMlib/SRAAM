# SRAAM ver.2

SRAAM ver.2 (Same Risk Area Assessment Model) is a tool designed to support decision makers in identification and delineation of a Same-Risk-Area (SRA). An SRA is a marine area within which marine vessels operators (e.g. ferries, offshore supply ships, etc.) may be granted an exemption to the Ballast Water Management Convention (BWMC) that require ship owners to treat the ballast water before recharging ballast water into the marine environment. The primary objective of of the BWMC is to reduce the risk of introducing marine invasive species, and in case of any exemption granted by national authorities a Risk Assessment needs to be carried out. Details can be found in the G7 guideline of the BWMC. A key component of such a risk assessment is to understand how marine invasive species may disperse due to natural processes. If an organisms is believed to disperse efficiently within an area the additional risk from ballast water mediated transfer may be negligible.

The SRAAM tool is used to calculate the dispersal trajectories of agents representing individual marine pelagic larvae or pelagic lifestages of a marine organism. From simulated agent trajectories, connectivity matrices are computed and cluster analyses are done, this way identifying marien regions where the connectivity within each region is high, and where connectivity between regions are low. The strength of within and between regions connectivity together with other types of relevant information can be used to support decission makers in whehter or not to assign an SRA.

The tool utilizes a combination of 3 freeware programs:
 * Netlogo – which is one of the most popular software programs for AgentBased / Individualbased Modeling (Wilensky, U. 1999)
 * R – which is a popular software package for statistical and mathematical data analyses and processing (R Core Team 2013)
 * IBMlib – This is a modelling system (~model library) specifically developed for linking agentbased simulations to simulated 3D hydrodynamic data (Christensen 2008, Christensen et al. in review).

![](https://raw.githubusercontent.com/IBMlib/SRAAM/master/figures/sraam_concept.png)

Agent dispersal is calculated based on hydrographic data, i.e. data produced by simulation models describing ocean currents direction and speed. Results from the larvae dispersal calculation given a user specified simulation period with a desired number of agents representing pelagic larvae or lifestages of a marine organisme, can be displayed as an animation showing individual agent positions in space and time, and the trajectories followed by each agent throughout the simulation period. Biological parameters can be set prior to the dispersal simulation, including pelagic larvae duration (PLD), settling competency period (the time/age at which larvae achieve competence for settling), spawning time and duration, distribution of spawning and settling habitats and vertical migration and/or positioning of agents during migration. 

Once a dispersal calculation is done, the connectivity of the marine area can be analyzed. The user can specify a grid with any specified resolution (e.g. 20x20 = 400 subareas) and all information from simulated agent trajectories (~start and end positions) stored in the simulation result file (ncdf format) will be compiled into a matrix summarizing the pairwise connectivity probability between all pairs of sub-areas (e.g. 400 x 400 matrix). The connectivity probability represents the probability that an agent spawning, or released, in one area will settle in any of the other areas within the model domain.

The connectivity matrix can be further analyzed using cluster analyses, to identify clusters of subareas where connectivity between subareas are high, and where connectivity to neighboring clusters are low. These cluster analysis results are here referred to as hydrographic regions, and is one of the primary outputs of the SRAAM tool that can support the identification and delineation of a Same-Risk-Area. The individual steps involved in the identification of hydrographic regions using the SRAAM tool are shown in Figure 1.

This version of SRAAM support 4 types of hydrographic data formats for agent dispersal simulation include (more to come):

- HBM (North Sea and the Western Baltic Sea)
- POM (The North Sea)
- NEMO (Mediterranean)
- NCOM (Caribbean)

In additaion the SRAAM tool comes with a bootstrapped testing configuration based on the ECOSMO physical-biogeochemical model with a single time frame repeated over time to provide testing environment where hydrographic data processing is minimal. All data must inlcude current speed and direction, water temperature and salinity. 

Any bugs please report to Flemming Thorbjørn Hansen (ftho@aqua.dtu.dk) or Asbjørn Christensen (asc@aqua.dtu.dk).


