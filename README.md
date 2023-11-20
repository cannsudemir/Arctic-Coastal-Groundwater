README
=======================================

The data in the given spreadsheets is published as a supplementary information to the article named
"Supra-permafrost aquifers of the Arctic coast and their significant groundwater, carbon, and nitrogen fluxes"
by Demir, C., McClelland, J. W., Bristol, E., Charette, M. A., Cardenas, M. B.

This document is aimed to give information on the data provided and how they are tied to the related manuscript.

Piezometer_information.csv
------------------
This data was used in the making of Figure 2 and S6. Units are given in meters.


Detailed piezometer information on shore-perpendicular transects in Simpson Lagoon (SL A & B) and Kaktovik Lagoon (KL) shown in Figure 1.


Temp-depth-sensor_information.csv
------------
This data was used in the making of Figure 2 and S6. Units are given in meters.

Detailed information temperature-depth sensor setup installed along the shore-perpendicular transects in SL(A & B) and KL.


temperatures.csv
-------------

This data was used in the making of Figures 2, S7, S8 and S9.

Temperatures measured at multi-depth (depth-below-ground or elevation w.r.t. local reference point is given in meters) sensors at their pair piezometer locations in our sites at KL and SL.


Inverted-resistivity_SL.csv
---------------------

This data was used in the making of Figures 2, S1, S2 and S3.

True Resistivity (ohm.m):
The apparent resistivity data (also provided as .stg and .dat files for AGI and Res2dinv softwares, respectively) is inverted to true resistivity.

x (m):
Horizontal distance

z (m):
Vertical distance	

LB_underwater_Schlumber:
Lagoon bottom Schlumberger survey. Underwater inversion was completed in AGI EarthImager 2D software. The provided data includes the assigned lagoon cells, therefore it is not showing the true lagoon bottom topography. See the topographic information given in underwater_LB.uwt file.

SP_Schlumberger-DD_w/topo:
Shore parallel merged (Schlumberger+Dipole-dipole) survey. The inversion was completed in RES2DINV software. Provided data includes topography.

TB_Schumberger-DD_w/topo:
Tundra merged (Schlumberger+Dipole-dipole) survey. The inversion was completed in RES2DINV software. Provided data includes topography.


HKs_grainsize_Ksat.csv
--------

This data was used in the making of Figure S11 and Table S5.

Hydraulic conductivity (HK, m/d) values estimated with various different methods, explained in the Supplemental Information document of the publication.

Saturated hydraulic conductivity of undisturbed sediment samples collected in Simpson Lagoon (SL), AK were measured via constant head tests (with and instrument called KSAT by METER.

Grain size distribution of disturbed sediment samples collected in Kaktovik Lagoon (KL), AK were measured via CAMSIZER particle analyzer. This data was then used to calculate HKs with empirical equations (i.e. Kozeny Karmen, Hazen, Beyer and Terzaghi).


Gw_head_salinity.csv
--------

This data was used in the making of Figure 3.

Measurements of total groundwater head (m) and salinity (given as specific conductance, S/cm) w.r.t. local reference elevation.
Given groundwater head values were corrected according to local air pressure and manual grounwater level measurements.


Lagoon_level_salinity.csv
--------

This data was used in the making of Figure 3.

Measurements of lagoon level (m) and salinity (given as specific conductance, S/cm) w.r.t. local reference elevation.
Given lagoon level values were corrected according to local air pressure (and sea surface level in SL) measurements.


GW_flux_via_num_models.csv
--------

This data was used in the making of Figure 4.

Description: Values are given for the upward discharge estimated for 100 different hydraulic conductivity (HK) scenarios and integrated over the top boundary of the model domain. They were calculated with the "Line Integration" tool in COMSOL software, with the expression "dl2.v*(dl2.v>0)" and unit of m3/day/m (dl2.v is in m/day). It was then multiplied by 1000 m/km to get a unit of m^3/day per km.


GW_flux_via_heat-tracing.csv
--------

This data was used in the making of Figures 3, 4, S10, S12 and S13.

Vertical groundwater flux (m/d) estimated via FLUX-LM (Kurylyk, B. L. et al. (2017)): Flux for each timestep of temperature-depth measurement is calculated assuming steady-state temperature-depth profile at each time step and a uni-layer system. This approach is not meant to estimate transient fluxes, rather is to give an idea about daily averages. Therefore, results in the main text were not reported as time series, instead, they were given as daily averages. Fluxes along the transects estimated in m/d were then integrated over the seepage length to find the total fresh groundwater discharge. See Methods and the SI of the article for details.

REFERENCES:
Kurylyk, B. L. et al. Heat as a groundwater tracer in shallow and deep heterogeneous media: Analytical solution, spreadsheet tool, and field applications. Hydrol. Process. 31, 2648\'962661 (2017).


GW_flux_via_Darcys_law.csv
--------

This data was used in the making of Figures 3, 4, S10, S12 and S13.

Vertical groundwater flux (m/d) estimated via Darcy's Law.


deltaH:
head difference between lagoon and groundwater

deltaz:
vertical distance between seabed elevation and piezometer measurement elevation
fittedHK:
hydraulic conductivity estimated by graph fitting (HeatTracing-vs-DarcysLaw)


COMSOL_model_files
--------

The list of files given in this folder are to reproduce groundwater flux estimates via numerical models. COMSOL files (.mph) are provided for each model domain (SL and KL). initcond_1 and inittemp_1 .txt files are the steady-state concentration and temperature distributions which were previously calculated and are defined in the models as an initial state to run the scenarios.

ERT_data
--------

In this folder, all the raw ERT survey data (apparent resistivity, pre-inversion) for each transect surveyed are given for reproducibility.

