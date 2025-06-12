# Data science project

**Course:** Data Science Project (NWI-IBC045)

**Date:** June 2025

## Project description

The Jupyter notebooks in this repository process a partial dataset of the Veilig op School project (VOS; Behavioral Science Institute, Radboud University, Nijmegen, the Netherlands). They combine survey responses and movement tracking data of elementary school students and teachers to answer the following research question: *How do explicit and implicit measurement of teacher movement relate to the teacher-student relationship in the classroom?*    

### Hypotheses
* **Hypothesis 1:** Higher IOP positively correlates with higher STRS and SPARTS.
* **Hypothesis 2:** Higher IOP positively correlates with closer proximity.
* **Hypothesis 3:** Higher implicit proximity (XYZ) correlates with higher STRS and SPARTS.

## TO DO
### Import data
All raw files are stored on RU-hosted workgroup folder 
#### Tracking data
Variables: Timestamps, XYZ coordinates, TagId
#### Survey data
* Teacher variables: IOP, STRS
* Student variables: SPARTS
### Pre-processing
* **Tracking data**
  * [x] Add 'school' and 'class' values from subfolder name as key values
  * [x] Remove outliers
  * [x] Determine class breaks according to observation schemes and remove corresponding timestamps from the data (do not fill them in as empty) 
  * [x] Fill in missing timestamps--tracker goes to sleep mode after 3min of not moving
  * [x] Determine tracking start and end time--check observer logbooks!
### Survey data
  * [x] Calculate scores: check codebook for sources on correct computation
  * [x] Extract IOP scores from teacher responses
  * [x] Match individual IOP responses to student IDs
  * [x] Extract STRS scores from teacher responses
  * [x] Extract SPARTS scores from student responses
### Processing
  * [x] Compute Euclidean teacher-student distance
  * [x] Determine baseline teacher-student distance
  * [x] Compute how many times teacher approached student and vice-versa
### Analysis
  * [x] Regression analysis tracking data vs survey scores
    * IOP scores vs times approached -> check if IOP matches XYZ
    * Detailed IOP responses not relevant (why the teacher chose (not) to approach)
  * [x] Regression analysis survey vs survey scores
    * IOP vs STRS
    * IOP vs SPARTS

## Acknowledgements
This project uses the [apa.mplstyle](https://github.com/sollan/apa.mplstyle?tab=readme-ov-file#GPL-3.0-1-ov-file) stylesheet by [@sollan](https://github.com/sollan), licensed under GPL-3.0.