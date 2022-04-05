# Projectfiles
Files for Dolphin Vocalization and Sighting Correlation Analyses 

Project objective:
To understand the relationship between dolphin sightings and vocalizations within 5-10 minutes of the sighting (acoustic recorders set to record for 2 min every 20 minutes).

To see if with greater dolphin sight density do we also witness greater vocalization density, when we only have passive acoustics to rely on are many vocalizations a good indicator that there are many dolphins present.

Summed monthly across stations for vocalizations and sightings to look at seasonal patterns. 

Model: generalized linear model with guassian distribution, log+1 transform of dolphin count and vocalization count.

Response variable: Dolphin count
Explanatory variables: Total vocalization count, echolocation count, burst pulse count, or whistle count
Categorical factors: Season, Site
Continuous factors: Calf count, Fish calling score sums for each fish species that choruses (toadfish, silver perch, spotted seatrout, and red drum).

