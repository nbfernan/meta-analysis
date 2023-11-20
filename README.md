# meta-analysis

This repository houses R scripts that are companions to the meta-analysis described in Fernandez (2023). 

[CITATION HERE]

## Abstract
Increasing global use of dams is a major threat to freshwater ecosystems as they dramatically disrupt river flow regimes resulting in a cascade of negative impacts on fish and other aquatic biota. Quantitative reviews of damming impacts have focused on community level responses, but a synthetic understanding of species-specific effects remain unclear. Such work is needed because freshwater fishes are among the most diverse clades in the animal kingdom, possessing a wide variety of life history traits that may facilitate resiliency in the face of increasing damming worldwide. To help fill this knowledge gap, we conducted a meta-analysis to evaluate whether key life history traits mediate fish population response to damming. We developed linear mixed models to evaluate if migration status, body size, reproductive strategy, trophic level, and taxonomy influence population response to damming. Overall, we observed both negative and positive population responses to damming suggesting that there is no universal response to this type of disturbance. Further, there was no single or combination of life history trait(s) that significantly explained variation in our models. There was weak evidence that maximum body length and parental care through nest guarding influenced the response of fish to damming. Taxonomic analysis revealed a single order, Eupercaria, that exhibited some evidence of positive response to damming. Overall, our findings suggest that dams create both positive and negative effects on fish populations without a clear signal from the life history traits we evaluated. The ability to counter the effects of damming likely depends on complex interactions among traits not measured in our analysis and other site-specific factors that result in population increases or declines. As such, case-by-case system assessments are likely still needed to understand and predict how different species of fishes respond to dams, especially given the increased use of dams in some parts of the world.  


## File descriptions
1.	`Data_extraction_full_v7.csv` – Primary dataset that includes extracted data from papers. 
2.	`migration_data_final.csv` – small dataset of species where migration status is included.
3.	`01_rfishbase_mergeddata_Nov.3.2021.csv` – This csv file is written at the end of the `01_Data_extraction_Fishbase.R` script. This file contains the data retrieved from Rfishbase and migration status files merged in. This file is timestamped for data retrieval from RFishbase on Nov 3, 2021.  
4.	`02_explored-data_Nov.4.2021.csv` – This csv file is written at the end of the `02_Data_exploration. R` script. Life history traits are identified to move forward with and filtered to include complete cases of these traits to include in the model (i.e., no NAs present in particular trait data). 
5.	`03_final_dataset_Nov.4.2021.csv` – This csv file is written at the of the `03_Data_cleaning.R` script. After data is cleaned and the effect size is calculated. This is the data file we use to move forward in the remainder of the downstream scripts (i.e., scripts 04-06). 
6.	`01_Data_extraction_Fishbase.R` – A workflow of extracting trait data and other exploratory variables from RFishbase. 
7.	`02_Data_exploration. R` – Explore the relationships between trait variables and response data, including the variation of traits to determine if they should be included in the linear mixed model. 
8.	`03_Data_cleaning.R` – Clean the data and calculate effect sizes for downstream use.
9.	`04_Effect-size_exploration.R` – Using the trait data, explore the relationships between effect sizes and independent variables.
10.	`05_Modelling.R` – First, perform a linear mixed model using response data (population abundances) with fixed (life history traits) and random effects. Second, perform a linear mixed model using response data and taxonomic order as a fixed effect with random effects. Explore residuals and other influences on our model results, including outliers. 
11.	`06_Figures.R` – Figures generated for the in-text and supplementary materials of the Fernandez et al., (2023) publication.
