# SRAAM ver.2

SRAAM ver.2 (Same Risk Area Assessment Model) is a tool designed to support decision makers in identification and delineation of a Same-Risk-Area (SRA). An SRA is a marine area within which marine vessels operators (e.g. ferries, offshore supply ships, etc.) may be granted an exemption to the Ballast Water Management Convention (BWMC) that requires ship owners to treat the ballast water before being recharged into the marine environment. The primary objective of the BWMC is to reduce the risk of introducing marine invasive species, and before any exemption can be granted by national authorities a Risk Assessment needs to be carried out. Details can be found in the G7 guideline of the BWMC. A key component of such a risk assessment is to understand how marine invasive species may disperse due to natural processes. If an organisms is believed to disperse efficiently within an area the additional risk from ballast water mediated transfer may be negligible.

The SRAAM tool is used to calculate the dispersal trajectories of agents representing individual marine pelagic larvae or pelagic life stages of a marine organism. From simulated agent trajectories, connectivity matrices are computed and cluster analyses are done, this way identifying marine regions where the connectivity within each region is high, and where connectivity between regions are low. The strengths and directions of within and between regions connectivity together with other types of relevant information can be used to support decision makers in whether or not to assign an SRA.
The tool utilizes a combination of 3 freeware programs:

•	Netlogo – which is one of the most popular software programs for Agent-Based / Individual-based Modeling (Wilensky, U. 1999)

•	R – which is a popular software package for statistical and mathematical data analyses and processing (R Core Team 2013)

•	IBMlib – This is a modelling system (~model library) specifically developed for linking Agent-Based simulations to simulated 3D    hydrodynamic data (Christensen 2008, Christensen et al. in review).
 
Agent dispersal is calculated based on hydrographic data, i.e. data produced by simulation models describing ocean currents direction and speed, water temperature and salinity. Results from the agent dispersal calculation given a user specified simulation period with a desired number of agents representing pelagic larvae or life stages of a marine organism, can be displayed as an animation showing individual agent positions in space and time, and the trajectories followed by each agent throughout the simulation period. Biological parameters can be set prior to the dispersal simulation, including pelagic larvae duration (PLD), settling competency period (the time/age at which larvae achieve competence for settling), spawning time and duration, distribution of spawning and settling habitats and vertical migration and/or positioning of agents during migration.

Once a dispersal calculation is done, the connectivity of the marine area can be analyzed. The user can specify a grid with any specified resolution (e.g. 20x20 = 400 subareas) and all information from simulated agent trajectories (~start and end positions, and experienced salinity and temperature extremes) stored in the simulation result file (ncdf format) will be compiled into a matrix summarizing the pairwise connectivity probability between all pairs of sub-areas (e.g. 400 x 400 matrix). The connectivity probability represents the probability that an agent spawning, or released, in one area will settle in any of the other areas within the model domain. Finaly the cluster analysis identifies hydrographic regions where connectivity within regions are high, and connectivity between regions are low. Multiple generations connectivity analysis and hydrographic region delineation is supported.
The individual steps involved in the identification of hydrographic regions using the SRAAM tool are shown in Figure 1.
This version of SRAAM support 4 types of hydrographic data formats for agent dispersal simulation include (more to come):

•	HBM (North Sea and the Western Baltic Sea)

•	POM (The North Sea)

•	NEMO (Mediterranean)

•	NCOM (Caribbean) 

In addition the SRAAM tool comes with a bootstrapped testing configuration based on the ECOSMO physical-biogeochemical model with a single time frame repeated over time to provide testing environment where hydrographic data processing is minimal. All data must include current speed and direction, water temperature and salinity. 

Any bugs please report to Flemming Thorbjørn Hansen (ftho@aqua.dtu.dk) or Asbjørn Christensen (asc@aqua.dtu.dk).

