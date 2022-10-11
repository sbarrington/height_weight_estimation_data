# Forensic Height and Weight Estimation Dataset

## README file
Collected and curated by Hany Farid and Sarah Barrington, October 2022.

## Overview
This dataset comprises actual and estimated height and weight measures for a range of estimators and settings. The data is anonymised and spans 1145 unique images and 58 image participants.

There are two separate CSV tables included in the dataset:   
1. <b>height_weight_combined_estimates.csv</b> - images with their particpant's actual height and weight measures, alongside each of the four estimators described below.  
2. <b>height_weight_mturk_responses.csv</b> - the full responses from the Amazon Mechanical Turk (MTurk) study participants. 

Below are the settings and estimators used, alongside their corresponding numeric coding across both tables.    

<b>Settings:</b>  
* '1' - in-the-wild - participants are situated in a real-world corridor with door frame.  
* '2' - reference-free studio - participants stand against a plain white background with no reference object.  
* '3' - reference object studio - participants stand against a plain white background next to a reference object.  

<b>Estimators (groups):</b>   
- '1' - experts - estimates provided by professional photogrammetrists.  
- '2' - AI - estimates computed through the fitting of a 3D model to the image, as described in the body of the paper.  
- '3' - baseline - estimates computed through guessing the gender-specific population mean for each participant.  
- '4' - non-expert estimator data for both crowd and individuals - with errors computed through either a) taking the median estimate for an image and using this to calculate error, or b) taking the median error by image as described in the body of the paper.   

## Combined Estimates Table
The height_weight_combined_estimates.csv file provides the full list of photos used across all settings.

<b>Keys:</b>  
* image	- unique image identifier.  
* image_participant_id - unique identifier for participants in images.  
* setting	- as described above (1-3).  
* group	- estimator, as described above (1-4).  
* estimated_height_cm - corresponding height estimation in centimeters.	  
* estimated_weight_kg - corresponding weight estimation in kilograms.  	
* height_cm	- image participant's actual height, measured in centimeters.  
* weight_kg - image participant's actual weight, measured in kilograms.  


## MTurk Responses Table
The height_weight_mturk_responses.csv table provides the raw responses from MTurk prior to aggregation and error calculation.   

<b>Keys:</b>    
* image	- unique image identifier.  
* image_participant_id - unique identifier for participants in images.	  
* setting	- as described above (1-3).  
* mturk_participant_id - the unique identifier of the MTurk respondent.	  
* estimated_height_cm - the height estimated by the given MTurk respondent for the participant photographed in the image, in centimeters.	  
* actual_height_cm - image participant's actual height, measured in centimeters.  	
* estimated_weight_kg - the weight estimated by the given MTurk respondent for the participant photographed in the image, in kilograms.  
* actual_weight_kg - image participant's actual weight, measured in kilograms.  

## Contact
For further data inquiries, please contact sbarrington@berkeley.edu.



