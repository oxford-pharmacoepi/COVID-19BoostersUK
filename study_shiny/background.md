-----
# This block contains the metadata of the `.md` document. You can add here:
#   - background keys: header, footer.
#   - bslib::card arguments.
# You can find more information on how to use this section in the background vignette.
# header: ""
-----

This Shiny app presents results from COVID-19 booster vaccination campaigns conducted in Autumn 2023, Spring 2024, Autumn 2024, Spring 2025, and Autumn 2025.

The app was developed with the Shiny package. On the one hand, it helps assess the research readiness of a set of cohorts by displaying their data validity and key descriptive characteristics. On the other hand, it facilitates review by the different people involved in the study design by bringing together all study outputs in one place.

This assessment, combined with careful manual refinement, results in the final Shiny app. It includes the following sections:

- **Summary**  
  Collects the imported results and provides both the type of summary and their internal structure.

- **OmopSketch**  
  Contains information about the database.
  - **Snapshot:** Helps to better understand the database in which the cohorts were created. This includes descriptive features such as the database name and size, as well as operational characteristics such as the date or source of the extracted information.
  - **Observation period Summary:** Table and plot assessing the patient's observational information available in the database.

- **Objective 1: Cohort Characterisation**  
  Provides information about the study population in each cohort in the database, identified in the **CDM name** widget.
  - **Cohort Attrition:** Summarises the inclusion and exclusion criteria for both records and subjects, helping determine whether individuals should be considered part of the cohort. The tables and diagrams are provided for all vaccinated individuals (“Vaccinated records of the overall population”), “Eligibles for individuals”, and “Vaccinated eligibles”. The cohort of interest should be selected in the **Table name** widget, and the campaign of interest for the latter two should be selected in **Cohort name**. Note that the first is not restricted to campaigns and therefore corresponds to “Covid vaccine”. The **Variable name** widget controls whether the inclusion or estimate criteria apply to records, subjects, or both. The table can be manually adjusted for easier visualisation.
  - **Cohort Characteristics:** Combines a table and a plot to visualise the selected characteristics for vaccinated eligible individuals and eligible individuals. These should be selected in the **Table name** widget on the left. Results are shown for the selected campaigns in **Cohort name**, together with the corresponding estimates. Once the estimate name is identified in the table, the respective **Estimate name**, **Variable name**, and matching plot can be selected to visualise the result.
  - **Vaccinated Characteristics:** Plots the number of vaccinated eligibles from “Vaccinated eligibles” for the selected campaigns in **Cohort name**, using the strata selected in the **Strata to use** widget.
  - **Vaccination Chronology:** Contains three panels for COVID-19:
    1. **Overall vaccine administration:** Number of vaccines administered over time in the database, by dose.
    2. **Vaccinated eligibles in booster campaigns:** Number of booster doses among vaccinated eligibles across the four campaigns, by dose.
    3. **Cumulative vaccination chronology overall:** Cumulative number of vaccines over time in the database, by dose 

- **Objective 2: Coverage**  
  Displays booster vaccination coverage estimated for the selected estimate in **Estimate name** across sociodemographic groups, separately for each campaign of interest among eligibles.
  - **Summarise Table:** Contains summaries of the “Eligibles for vaccination” cohort for each selected strata sublevel (Region, TDI, Sex, Immunosuppressed, Age group, Age eligibility, Overall) and for the selected campaigns in **Cohort name**, presented either as Tidy or as a Table. Both tables allow manual adjustment for visualisation.
  - **Vaccinated Characteristics:** Plots the coverage of vaccinated eligible individuals, estimated from the "Vaccinated eligibles" cohort for the selected campaigns in **Cohort name** and the selected strata in **Strata to use**.

- **Objective 3: Associated factors**  
  Within eligible individuals, factors associated with receipt of a booster vaccination are estimated independently for each campaign of interest, while accounting for sociodemographic characteristics. Both the combined and sequential models are included.

- **Logs**  
  Illustrates the study workflow and the time allocated to each step, both in a table and in a plot.

<p style="text-align: right;">
  <img src="hds_logo.png" width="100px">
  <img src="ohdsi_logo.svg" width="100px">
  <img src="shiny.svg" width="100px">
</p>


