# Methods

*I added an RQ and some hypotheses because we need a specific goal instead of just digging around in data. I didn't think about these much so please add to them and refine them.--MC, 11-04-2025*  

**RQ:** How do explicit (IOP) and implicit (XYZ coordinates) measurement of teacher movement relate to student-teacher relationships (STRS, SPARTS)?

**Hypothesis 1:** Higher IOP positively correlates with higher STRS and SPARTS.

**Hypothesis 2:** Higher IOP positively correlates with closer proximity. 
* *But how are we going to define proximity? Maybe determine a range for how many times a day teacher approached student (also need to determine how long they need to stay next to the student to count as approaching), and how much time total the teacher spent close to student?--MC, 11-04-2025*

**Hypothesis 3:** Higher implicit proximity (XYZ) correlates with higher STRS and SPARTS.

## TO DO

*Add or remove steps according to need.*

### Import data
* **Tracking data**
    * Raw CSV files stored in /WRKGRP/STD-FSW-BSI-SD-Movement_Tracking/dsp/data/tracking
    * Variables: Timestamps, XYZ coordinates, TagId
* **Survey data**
    * Teachers: IOP, STRS
    * Student: SPARTS
### Pre-processing
* **Tracking data**
    * Add 'school' and 'class' values from subfolder name as key values
    * Remove outliers
    * Fill in missing timestamps -> tracker goes to sleep mode, see VU paper for method
    * Determine tracking start and end time
* **Survey data**
    * Calculate scores: check codebook for sources on correct computation
      * We need to ask for scoring sheets for both SPARTS and STRS!
    * Check for weird data (they're reliable scales so I guess it should be fine--MC, 11-04-2025) 
* ...
### Processing
* Compute Euclidean teacher-student distance -> see VU paper for method
* Determine baseline teacher-student distance
    * *see Carlijn's source for initimate/personal/social space*
* Compute how many times teacher approached student and vice-versa
    * *Determine what approaching means--entering personal space, or social space? -- Maja, 25-04-2025*
    * *If we're comparing IOP scores (how many times a teacher thinks they approached a student), we also need to make sure we've determined that the teacher approached the student, not the other way around -- Maja, 25-04-2025*
* ...
### Analysis
* Regression analysis tracking data vs survey scores
    * IOP scores vs times approached -> check if IOP matches XYZ
* Regression analysis survey vs survey scores
    * IOP vs STRS
    * IOP vs SPARTS
* ...

## LOGBOOK

11-04-2025
* created new file structure in workgroup folder
* loaded and inspected available data in Jupyter
* determined and requested missing data
25-04-2025
* set up Github repository
* 