# University of Oregon Survey of Health and Well-being (SHWell)

This repository contains code related to the SHWell study. 

## Participants
Participants were 636 undergraduate students at the University of Oregon, enrolled in a psychology or linguistics course. This study was approved by the University of Oregon Institutional Review Board. Participants consented to participate in this study by clicking the button to continue the survey and received course credit for participation.

## Data quality and exclusion criteria
Participant responses were excluded if they did not appear to have been completed in good faith. To determine what constitutes a "good faith" response, we developed the following exclusion criteria based on the analyses conducted in `data_cleaning.Rmd`:
* completion of 2% or less of the survey  
* incomplete duplicate responses  
* responses faster than 16 minutes  
* responses slower than 48 hours  

Based on these criteria, 40 participant responses were excluded. 

Although we did not exclude participants based on response invariance, we include the following two measures of invariance that researchers can use to exclude participants:
* `sd_questionnaire` = standard deviation for each questionnaire  
    * If questionnaire was not completed, `sd_questionnaire = NaN`  
    * If questionnaire is a single item, `sd_questionnaire = NA`  
* `percent_survey_invariant` = percent of the survey (across all questionnaires > 1 item completed) that have no variance (SD = 0)
