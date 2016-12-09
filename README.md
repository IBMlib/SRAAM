# SRAAM

SRAAM (Same Risk Area Assessment Model) is a tool that calculates dispersal trajectories of agents representing individual marine pelagic larvae and provide same risk areas based on cluster analysis of the larval habitat connectivity matrix computed from dispersal trajectories.

The tool utilizes a combination of 3 freeware programs:
 * Netlogo – which is one of the most popular software programs for AgentBased / Individualbased Modeling (Wilensky, U. 1999)
 * R – which is a popular software package for statistical and mathematical data analyses and processing (R Core Team 2013)
 * IBMlib – This is a modelling system (~model library) specifically developed for linking agentbased simulations to simulated 3D hydrodynamic data (Christensen 2008, Christensen et al. in review).


Larvae dispersal is calculated based on hydrographic data, i.e. data produced by simulation models describing ocean currents direction and speed. Results from the larvae dispersal calculation given a user specified simulation period with a desired number of agents representing pelagic larvae, can be displayed as an animation showing individual larvae positions in space and time, and the trajectories followed by each larvae throughout the simulation period. The animation of simulated larvae can be shown together with data on bathymetry (from the Hydrographic data set) and land boundaries (from a GIS file). Biological parameters can be set prior to the dispersal simulation, including pelagic larvae duration (PLD), settling competency period (the time/age at which larvae achieve competence for settling), spawning time and duration, and distribution of spawning and settling habitats.
Once a dispersal calculation is done, the connectivity of the marine area can be analyzed. The user can specify a grid with any specified resolution (e.g. 20x14 = 280 subareas) and all information from simulated larvae trajectories (~start and end positions) stored in the simulation result file will be compiled into a matrix summarizing the pairwise connectivity probability between all pairs of sub areas (e.g. 280 x 280 matrix). The connectivity probability represents the probability that an agent spawning, or released, in one area will settle in any of the other areas within the model domain.
The connectivity matrix can be further analyzed using different types cluster analyses, to identify clusters of subareas where connectivity between subareas are high, and where connectivity to neighboring clusters are low. These cluster analysis results are here referred to as hydrographic regions, and are the primary outputs of the SRAAM tool that can support the delineation of a SameRiskArea. The individual steps involved in the generation of hydrographic regions using the SRAAM tool are shown in Figure 1.
Notice that alternative to a regular grid of say 20x14 subareas for the connectivity analysis, separate areas representing spawning and settling habitats respectively can be specified if required. This is not yes supported by the user interface but can be done by manually modifying a simulation parameter file using a text editor.
As a prototype this version only support 2 types of hydrographic data for larvae dispersal simulation,  one consisting of a hydrographic data set with current speed and direction varying in space, but constant in time (for demonstration purposes),  and one data type identical to the format of the HBM hydrographic data set for the North Sea, the inner Danish straits and the Western Baltic sea (source: Danish Meteorological Institute  DMI) used as a show case for documenting the use of the tool on a realistic but limited data set. Details of the supported formats in this prototype are described the section “Hydrographic data”.

The animation of simulated larvae trajectories is mostly an option available for visualizing the dispersal patterns and drivers in the system analyzed, and should only be done using simulation results for relatively limited number of agents , e.g. ~ 100  1000 agents for 1 year simulation, due to pcprocessing time and optimal visualization.
