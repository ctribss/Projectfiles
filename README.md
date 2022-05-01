# Projectfiles
Dolphin Vocalization and Sighting Analyses 

Project objective:
To understand the relationship between dolphin sightings and vocalizations and what may be  influencing  dolphin vocalizations over space and time. 
If we see a positive relationship between dolphin vocalizations and the number of dolphins we can infer call density is positively correlated to dolphin abundance. Passive acoustic monitoring and visual boat-based surveying were conducted jointly to understand spatial and temporal patterns in dolphin vocalizations and sighting abundance. 
Important to understand how acoustic vs visual monitoring may differ in abundance estimates and whether passive acoustics can overtime replace visual survey methods for certain research questions.

Structure of Code Base:

Project working directory:
Main project broken into 4 folders: data, scripts, figs, and presentations

data folder (): Contains raw data file (raw_sighting_data) and files to be used in analysis (bimonthly)
  - raw_sighting_data.csv : contains all sighting/vocalization data before any summarizing 
  - raw_sighting_data_sumrytbles : tables summaarizing vocalization and sighting patterns across site and season
  - bimonthly.csv : contains all sighting/vocalization data summed bimonthly at each station
  - dsite.csv : contains all sighting/vocalization data summed monthly at each station and was used in  
  'Dolphin_Vocal_and_Sighting_Analyses_Monthly.Rmd' same analyses at monthly time scale. Used to compare 
  to bimonthly if still see significance and we do, however was not included in graphs and figures in 
  final presentation and paper.
 
scripts folder ():
  - Dolphin_Vocal_and_Sighting_Analyses_Rough.Rmd : contains preliminary analyses (not used for final
  presentation or paper) 
  - Dolphin_Vocal_and_Sighting_Analyses_Final.Rmd : contains R code for final analyses at bimonthly scale, 
  cleaned up and annotated for reproducibility
  - Dolphin_Vocal_and_Sighting_Analyses_Monthly.Rmd : contains R code for same analyses at monthly scale,
  cleaned up and annotated for reproducibility (not used for final presentation or paper) 
  
figures folder (): 
Final figures to be used in report as well as supplemental figures.  

presentations folder (): 
Final presentations to be used for project pitch and for final presentation.


Additional Information/Details on Project and Data Analysis:

Methods

Study Area: Charleston Harbor 

Time range of study: Dec 11th 2017 to June 1st 2019

Passive acoustics:
-A total of six passive acoustic recorders were stationed in Charleston Harbor 
-Stations determined based on core use areas of the Charleston Estuarine System Stock determined by spatial analyses on historical photo-ID surveys and due to their locations within the harbor with stations A, B, C, and D all within the shipping channel while stations E and F are not and are more representative of recreational boat traffic
-Recorders are deployed for 3 months at a time then retrieved and acoustic files are manually analyzed to identify fish and dolphin vocalizations

Visual Surveying:
-Small vessel-based photo-ID surveys in Charleston Harbor that were conducted bimonthly within designated 2 km radius around each recording station. 
-Once dolphin(s) were observed, sighting data collected included GPS location, start and end times of sighting, group size estimates for dolphins, calves, and neonates (i.e., minimum, maximum, and best estimate), weather conditions, water depth (m), and water quality measurements using a YSI Handheld Multiparameter Instrument. 
-Water quality measures included water temperature, salinity, dissolved oxygen, and turbidity. 
-These vessel-based surveys were conducted under General Authorization for Scientific Research Letter of Confirmation No. 18859 issued by NMFS. 

 
Data analysis:
-Summed vocalizations and sightings across each survey (bimonthly) across stations.

Model: generalized linear models with gaussian distribution, log+1 transform of total vocalizations, echolocation, burst pulses, and whistles.

Response variable: Total vocalization count, echolocation count, burst pulse count, or whistle count
Explanatory variables: Total dolphin count
Categorical factors: Season, Site
Continuous factors: Calf count, Fish calling score sums for each fish species that choruses (toadfish, silver perch, spotted seatrout, and red drum).




