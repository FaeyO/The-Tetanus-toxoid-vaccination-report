# Who's Receiving the Tetanus Toxoid Vaccine (2019 -2023)

### Dashboard Link : https://public.tableau.com/views/GuardianShieldTetanusToxoidVaccinationSentinel/TetanusvaccinationDS?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link

## Problem Statement

Tetanus vaccination is a crucial preventive measure against tetanus, a serious bacterial infection caused by Clostridium tetani. The vaccine stimulates the body's immune system to produce antibodies against the tetanus toxin, providing immunity to the disease. It is typically administered as part of a combination vaccine, such as the DTaP vaccine for children or the Tdap vaccine for adolescents and adults. Routine vaccination is recommended to ensure ongoing protection against tetanus, particularly following injuries or wounds that may increase the risk of infection.

This dynamic dashboard offers a comprehensive overview of patient vaccination trends spanning 5 years. It enables healthcare providers to track and analyze patient attendance for Tetanus vaccinations, including those who have defaulted from taking the vaccine shots.

### Steps followed 

- Step 1 : Write SQL query to get data needed for analysis from the database.
- Step 2 : Data Cleaning and validation was carried to ensure data quality and intergrity is kept.
- Step 3 :  Save the cleaned and filtered data to a csv file.
- Step 4 :  Load the dataset into Tableau for visualizations..
- Step 5 : Create a calculated field to share the various age into categorical group.
- Step 6 : Create a calculated field to display both first and last names together. 
- Step 7 : Visual filters (Slicers) were added for easy visualization of Tetanus toxoid vaccination across the years. 
- Step 8 : Various  Visual like combo chart, line charts, map , Table and Area chart was used to show the various insights below;

  (a) Tetanus toxoid shot given by county

  (b) List of patient who have been actively taking the tetanus toxoid vaccine
  
  (c) Age category of Patient that the Tetanus vaccine were administered to.
  
  (d) Administration of Tetanus vaccination by Patient race 

  (e) Running total of Tetanus vacination
  

- Step 9 : In the report view, two text boxes were added to the canvas, to show the percentage of compliance of Patient with the Tetanus vaccination, and the total number of Tetanus vaccine given across the years (2019 - 2023).

- Step 10 : In the dashboard view, under the object tab, using using image option elements were added to the report design area. 

- Step 11 : An area chart was created to visualize the running total of Tetanus vaccine shots given across the 5 years.
        
- Step 12 : New measure was created to 

i. categorize age into groups.
    

Following Tableau expression was written for the same,
        
        Age_groups = IF [Age] >= 0 and [Age] <= 17 then '0-17' 
        ELSEIF  [Age] >= 18 and [Age] <= 35 then '18-35'
        elseif [Age] >=36 and [Age] <= 53 then '36-53'
        ELSEIF  [Age] >= 54 and [Age] <= 70 then '54-70'
        elseif [Age] >= 71 then '71+' 
        END

ii. create a name column from their first and last names.

        Name = First + ' ' + Last

 - step 13:        
A card visual was used to represent percentage of total compliance.

![TT_shot_given_page-0001](https://github.com/FaeyO/The-Tetanus-toxoid-vaccination-report/assets/118575325/d58b72ae-16f4-4e06-9083-7c933c7f58ad)

A card visual was used to represent total tetanus shot given

![TT_compliance_page-0001](https://github.com/FaeyO/The-Tetanus-toxoid-vaccination-report/assets/118575325/e26cb920-041f-4ad7-99dd-953656122f69)

 - Step 14 : The report was uploaded to the Tableau public server.
 
# Insights

A single page report was created on Tabeau, and the following inferences can be drawn from the dashboard;

### [1] Total Tetanus shot given  = 3481

### [2] Percentage of compliance = 35.4%

### [3] Patients aged 71 and above, along with those aged 18-35, accounted for the majority of attendees over the 5-year period.

### [4] There was a noticeable uptick in patient turnout overall, with a significant decline observed in 2023.
  
### [5] Patients from indigenous backgrounds constituted the smallest proportion (31%) of vaccinated individuals.
 


### Dashboard view

![Tetanus vaccination DS](https://github.com/FaeyO/The-Tetanus-toxoid-vaccination-report/assets/118575325/56d656b8-02fe-49b1-8c85-70e06a076421)


