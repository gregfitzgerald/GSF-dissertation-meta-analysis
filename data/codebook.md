# Codebook: Enrichment Meta-Analysis Data

## Data Files

- `rodent_data.csv` (115 columns)
- `human_data.csv` (134 columns)

---

## rodent_data.csv

### Study Identifiers

| Variable | Description |
|----------|-------------|
| `Article_ID` | Unique article identifier (LastNameYear format) |
| `Study_ID` | Study number within article |
| `Study_ID_Unique` | Globally unique study identifier |
| `Study_Arm_ID` | Unique study arm identifier for clustering |
| `Comparison_ID` | Unique comparison identifier |
| `Test_ID` | Test number within study |
| `Outcome_ID` | Outcome number within test |
| `Arm_Number` | Arm number within multi-arm studies |

### Bibliographic Information

| Variable | Description |
|----------|-------------|
| `Last_Name` | First author last name |
| `Year` | Publication year |
| `Title` | Article title |
| `Journal` | Journal name |
| `DOI` | Digital object identifier |
| `Citation` | Full citation |
| `Country_Of_Study` | Country where study was conducted |

### Sample Characteristics

| Variable | Description |
|----------|-------------|
| `Species` | Mouse or Rat |
| `Strain` | Strain name (e.g., C57BL/6, Sprague-Dawley) |
| `Sex` | Male, Female, or Both |
| `Sex_Distribution` | Percentage or description of sex distribution |
| `Age_At_Start_Days` | Age at intervention start (days) |
| `Control_N` | Sample size in control group |
| `Intervention_N` | Sample size in intervention group |
| `Enriched_N` | Sample size in enriched group (alias for Intervention_N) |

### RLS (Resource-Level Scale) Variables

| Variable | Description |
|----------|-------------|
| `RLS_Score_Control` | Total RLS score for control condition (0-11) |
| `RLS_Score_Intervention` | Total RLS score for intervention condition (0-11) |
| `RLS_Differential` | RLS_Intervention - RLS_Control |
| `Control_Group_RLS_Score` | Alias for RLS_Score_Control |
| `Intervention_Group_RLS_Score` | Alias for RLS_Score_Intervention |
| `Control_Group_RLS_Categories` | List of RLS categories present in control |
| `Intervention_Group_RLS_Categories` | List of RLS categories present in intervention |

#### Control Condition RLS Components (0 = absent, 1 = present)

| Variable | Description |
|----------|-------------|
| `Control_Social_Partners` | Social housing in control condition |
| `Control_Exercise_Wheels` | Running wheels in control condition |
| `Control_Wheel_Condition` | Wheel type/condition details |
| `Control_Additional_Space` | Extra floor space beyond standard |
| `Control_Shelters` | Hiding places/shelters |
| `Control_Nesting_Material` | Nesting material provided |
| `Control_Gnawing_Materials` | Chewable objects |
| `Control_Environmental_Complexity` | Platforms, tubes, climbing structures |
| `Control_Foraging_Opportunities` | Scattered food, foraging devices |
| `Control_Burrowing_Substrates` | Deep bedding for burrowing |
| `Control_Fresh_Plant_Matter` | Fresh vegetables, herbs |
| `Control_Sweet_High_Fat_Food` | Palatable food treats |
| `Quantity_Control_Social_Partners` | Number of cage mates |
| `Quantity_Control_Additional_Space_cm2` | Floor space in cm2 |

#### Intervention Condition RLS Components (0 = absent, 1 = present)

| Variable | Description |
|----------|-------------|
| `Intervention_Social_Partners` | Social housing in intervention condition |
| `Intervention_Exercise_Wheels` | Running wheels in intervention condition |
| `Intervention_Additional_Space` | Extra floor space beyond standard |
| `Intervention_Shelters` | Hiding places/shelters |
| `Intervention_Nesting_Material` | Nesting material provided |
| `Intervention_Gnawing_Materials` | Chewable objects |
| `Intervention_Environmental_Complexity` | Platforms, tubes, climbing structures |
| `Intervention_Foraging_Opportunities` | Scattered food, foraging devices |
| `Intervention_Burrowing_Substrates` | Deep bedding for burrowing |
| `Intervention_Fresh_Plant_Matter` | Fresh vegetables, herbs |
| `Intervention_Sweet_High_Fat_Food` | Palatable food treats |
| `Quantity_Intervention_Social_Partners` | Number of cage mates |
| `Quantity_Intervention_Additional_Space_cm2` | Floor space in cm2 |

### Intervention Characteristics

| Variable | Description |
|----------|-------------|
| `Intervention_Duration_Days` | Duration of enrichment in days |
| `Intervention_to_Test_Interval_Days` | Days between intervention end and cognitive testing |

### Regulatory Compliance

| Variable | Description |
|----------|-------------|
| `Canada_Post_2009` | Study conducted in Canada after 2009 guidelines |
| `EU_UK_Post_2010` | Study conducted in EU/UK after 2010 directive |

### Outcome Variables

| Variable | Description |
|----------|-------------|
| `Test_Name` | Name of cognitive test administered |
| `Test_Name_Standardized` | Standardized test category |
| `Cognitive_Domain` | Spatial, Recognition, Working Memory, Executive Function, Fear/Associative |
| `Variable_Name` | Specific outcome variable measured |
| `Variable_Value` | Value description |
| `Variable_Unit` | Unit of measurement |
| `Variable_Range_Min` | Minimum possible value |
| `Variable_Range_Max` | Maximum possible value |
| `Variable_Transformation` | Any transformations applied |
| `Direction` | Whether higher values indicate better (+1) or worse (-1) performance |

### Raw Outcome Data

| Variable | Description |
|----------|-------------|
| `Control_Group_Mean` | Mean outcome in control group |
| `Control_Group_Variance_Value` | SD in control group |
| `Control_Group_SD` | Standard deviation (control) |
| `Intervention_Group_Mean` | Mean outcome in intervention group |
| `Intervention_Group_Variance_Value` | SD in intervention group |
| `Enriched_Group_Mean` | Mean in enriched group (alias) |
| `Enriched_Group_SD` | SD in enriched group (alias) |
| `Variance_Source` | Source of variance estimate (reported, calculated, imputed) |

### Effect Size Variables

| Variable | Description |
|----------|-------------|
| `Hedges_g_corrected` | Hedges' g effect size (bias-corrected) |
| `sampling_variance_corrected` | Sampling variance (corrected) |
| `vi_adjusted_multiarm` | Final variance adjusted for multi-arm studies |
| `VIF_multiarm` | Variance inflation factor for multi-arm adjustment |

Note: Use `Hedges_g_corrected` and `vi_adjusted_multiarm` for analysis. These are the final effect sizes after all corrections.

### Multi-Arm Study Variables

| Variable | Description |
|----------|-------------|
| `Multi_Arm_Study` | Whether study has multiple arms (TRUE/FALSE) |
| `Number_of_Arms` | Total number of study arms |
| `Shared_Control_Group` | Whether control group is shared across comparisons |
| `Shared_Experimental_Group` | Whether experimental group is shared |
| `Control_Group_ID_Standardized` | Standardized control group identifier |
| `Intervention_Group_ID_Standardized` | Standardized intervention group identifier |
| `Control_Group_ID_Standardized_FIXED` | Corrected control group ID |
| `Intervention_Group_ID_Standardized_FIXED` | Corrected intervention group ID |
| `Total_Comparisons` | Total comparisons from this article |

### Risk of Bias (SYRCLE Tool)

| Variable | Description | Values |
|----------|-------------|--------|
| `SYRCLE_01_Sequence_Generation` | Random sequence generation | Low, Unclear, High |
| `SYRCLE_02_Baseline_Characteristics` | Similar baseline characteristics | Low, Unclear, High |
| `SYRCLE_03_Allocation_Concealment` | Allocation concealment | Low, Unclear, High |
| `SYRCLE_04_Random_Housing` | Random housing of animals | Low, Unclear, High |
| `SYRCLE_05_Blinding_Investigators` | Blinding of caregivers/investigators | Low, Unclear, High |
| `SYRCLE_06_Random_Outcome_Assessment` | Random outcome assessment | Low, Unclear, High |
| `SYRCLE_07_Blinding_Outcome_Assessment` | Blinding of outcome assessors | Low, Unclear, High |
| `SYRCLE_08_Incomplete_Outcome_Data` | Incomplete outcome data addressed | Low, Unclear, High |
| `SYRCLE_09_Selective_Outcome_Reporting` | Selective outcome reporting | Low, Unclear, High |
| `SYRCLE_10_Other_Sources_Bias` | Other sources of bias | Low, Unclear, High |
| `Overall_Risk_Of_Bias` | Overall risk of bias judgment | Low, Some Concerns, High |

### Data Provenance

| Variable | Description |
|----------|-------------|
| `Data_Source` | Where data was obtained (text, table, figure, supplement) |
| `Data_Extraction_Method` | How data was extracted (direct, WebPlotDigitizer, calculated) |
| `Morris_Method_Required` | Whether Morris method was needed for effect size |
| `Pre_Registration_Status` | Whether study was pre-registered |
| `Open_Data` | Whether data is openly available |

### Sensitivity Analysis Flags

| Variable | Description |
|----------|-------------|
| `exclude_main_analysis` | Exclude from main analysis (TRUE/FALSE) |
| `sensitivity_study` | Flagged for sensitivity analysis |
| `sensitivity_reason` | Reason for sensitivity flag |
| `any_sensitivity_flag` | Any sensitivity concern present |
| `sensitivity_age_violation` | Age outside inclusion criteria |
| `sensitivity_intervention_characteristics` | Atypical intervention |
| `sensitivity_statistical_issues` | Statistical concerns |
| `sensitivity_data_extraction` | Data extraction uncertainty |

---

## human_data.csv

### Study Identifiers

| Variable | Description |
|----------|-------------|
| `Article_ID` | Unique article identifier |
| `Study_ID` | Study number within article |
| `Study_ID_Unique` | Globally unique study identifier |
| `Study_Arm_ID` | Unique study arm identifier for clustering |
| `Comparison_ID` | Unique comparison identifier |
| `Test_ID` | Test number within study |
| `Outcome_ID` | Outcome number within test |
| `Arm_Number` | Arm number within multi-arm studies |

### Bibliographic Information

| Variable | Description |
|----------|-------------|
| `Last_Name` | First author last name |
| `Year` | Publication year |
| `Title` | Article title |
| `Journal` | Journal name |
| `DOI` | Digital object identifier |
| `Citation` | Full citation |
| `Publication_Type` | Type of publication |
| `Country_Of_Study` | Country where study was conducted |


### Sample Characteristics

| Variable | Description |
|----------|-------------|
| `Participant_Age_Mean` | Mean age of participants |
| `Participant_Age_Reported_Variance` | Reported variance in age |
| `Participant_Age_Reported_Variance_Type` | Type of variance (SD, SE, range) |
| `Participant_Age_Min` | Minimum participant age |
| `Participant_Age_Max` | Maximum participant age |
| `Participant_Sex` | Both, Male, or Female |
| `Sex_Distribution` | Percentage female |
| `Control_N` | Sample size in control group |
| `Intervention_N` | Sample size in intervention group |
| `Total_N` | Total sample size |

### Attrition and Analysis

| Variable | Description |
|----------|-------------|
| `Attrition_N` | Number of participants lost to follow-up |
| `Attrition_Rate` | Percentage attrition |
| `ITT_Analysis` | Intention-to-treat analysis used |
| `Per_Protocol_Analysis` | Per-protocol analysis used |
| `Intervention_Adherence` | Reported adherence rate |

### Intervention Characteristics

| Variable | Description |
|----------|-------------|
| `Intervention_Type` | Cognitive, Physical, or Multimodal |
| `Intervention_Description` | Detailed intervention description |
| `Intervention_Duration` | Duration value |
| `Intervention_Duration_Unit` | Duration unit (days, weeks, months) |
| `Intervention_Duration_Days` | Duration standardized to days |
| `Session_Duration_Value` | Minutes per session |
| `Session_Duration_Units` | Session duration unit |
| `Session_Frequency_Value_Per_Week` | Sessions per week |
| `Session_Count` | Total number of sessions |
| `Total_Hours` | Total intervention hours |
| `Supervised_vs_Unsupervised` | Supervision level |
| `Adaptive_Difficulty` | Whether difficulty adapts to performance |
| `Activity_Presentation` | How activity was presented (group, individual, computerized) |
| `Intervention_to_Test_Interval_Days` | Days between intervention end and testing |
| `Intervention_to_Test_Interval_Value` | Interval value |
| `Intervention_to_Test_Interval_Units` | Interval unit |

### Cognitive Training Details

| Variable | Description |
|----------|-------------|
| `Intervention_Type_Cognitive_Activity` | Type of cognitive activity |
| `Cognitive_Activity_Description` | Description of cognitive training |
| `Transfer_Distance_Classification` | Near, Far, or Very Far transfer |

### Physical Exercise Details

| Variable | Description |
|----------|-------------|
| `Intervention_Type_Physical_Activity` | Type of physical activity |
| `Physical_Activity_Description` | Description of exercise |
| `Exercise_Type` | Aerobic, Resistance, Combined, etc. |
| `Exercise_Intensity_Reported` | Whether intensity was reported |
| `Exercise_Intensity_Value` | Reported intensity value |
| `Exercise_Intensity_Category` | Light, Moderate, Vigorous |
| `Exercise_Intensity_Collapsed` | Simplified intensity category |

### Multimodal Intervention Details

| Variable | Description |
|----------|-------------|
| `Multimodal_Intervention_Status` | Whether intervention is multimodal |
| `Multimodal_Intervention_Description` | Description of multimodal components |

### Control Group Characteristics

| Variable | Description |
|----------|-------------|
| `Control_Group_Type` | Type of control (waitlist, active, no-contact) |
| `Control_Group_Description` | Description of control condition |
| `Control_Group_ID` | Control group identifier |
| `Control_Group_ID_Standardized` | Standardized control group ID |

### Outcome Variables

| Variable | Description |
|----------|-------------|
| `Test_Name` | Name of cognitive test |
| `Test_Name_Standardized` | Standardized test name |
| `Cognitive_Domain` | Executive Function, Spatial, Recognition, Working Memory, Processing Speed, Global Cognition |
| `Outcome_Name` | Specific outcome measured |
| `Component_vs_Calculation` | Whether outcome is component or composite |
| `Variable_Name` | Variable name |
| `Variable_Value` | Value description |
| `Variable_Unit` | Unit of measurement |
| `Variable_Range_Min` | Minimum possible value |
| `Variable_Range_Max` | Maximum possible value |
| `Variable_Transformation` | Any transformations applied |
| `Direction` | Whether higher values indicate better (+1) or worse (-1) performance |
| `Between_Or_Within_Design` | Study design type |

### Pre-Test Data

| Variable | Description |
|----------|-------------|
| `PRE_TEST_Control_Group_Mean` | Pre-test mean (control) |
| `PRE_TEST_Control_Group_Variance_Value` | Pre-test variance (control) |
| `PRE_TEST_Control_Group_Variance_Type` | Variance type (SD, SE) |
| `PRE_TEST_Intervention_Group_Mean` | Pre-test mean (intervention) |
| `PRE_TEST_Intervention_Group_Variance_Value` | Pre-test variance (intervention) |
| `PRE_TEST_Intervention_Group_Variance_Type` | Variance type (SD, SE) |
| `Control_PRE_Original_Variance_Type` | Original variance type (control) |
| `Intervention_PRE_Original_Variance_Type` | Original variance type (intervention) |

### Post-Test Data

| Variable | Description |
|----------|-------------|
| `POST_TEST_Control_Group_Mean` | Post-test mean (control) |
| `POST_TEST_Control_Group_Variance_Value` | Post-test variance (control) |
| `POST_TEST_Control_Group_Variance_Type` | Variance type (SD, SE) |
| `POST_TEST_Intervention_Group_Mean` | Post-test mean (intervention) |
| `POST_TEST_Intervention_Group_Variance_Value` | Post-test variance (intervention) |
| `POST_TEST_Intervention_Group_Variance_Type` | Variance type (SD, SE) |
| `Control_POST_Original_Variance_Type` | Original variance type (control) |
| `Intervention_POST_Original_Variance_Type` | Original variance type (intervention) |

### Change Score Data

| Variable | Description |
|----------|-------------|
| `CHANGE_SCORE_Control_Group_Mean` | Change score mean (control) |
| `CHANGE_SCORE_Control_Group_Variance_Value` | Change score variance (control) |
| `CHANGE_SCORE_Control_Group_Variance_Type` | Variance type |
| `CHANGE_SCORE_Intervention_Group_Mean` | Change score mean (intervention) |
| `CHANGE_SCORE_Intervention_Group_Variance_Value` | Change score variance (intervention) |
| `CHANGE_SCORE_Intervention_Group_Variance_Type` | Variance type |
| `Change_Score_Reported_Flag` | Whether change scores were reported |

### Effect Size Variables

| Variable | Description |
|----------|-------------|
| `Hedges_g_corrected` | Hedges' g effect size (bias-corrected, Morris dppc2) |
| `sampling_variance_corrected` | Sampling variance (corrected) |
| `vi_adjusted_multiarm` | Final variance adjusted for multi-arm studies |
| `VIF_multiarm` | Variance inflation factor for multi-arm adjustment |
| `calculation_method` | Effect size calculation method used |

Note: Use `Hedges_g_corrected` and `vi_adjusted_multiarm` for analysis. These are the final effect sizes after all corrections.

### Multi-Arm Study Variables

| Variable | Description |
|----------|-------------|
| `Multi_Arm_Study` | Whether study has multiple arms (TRUE/FALSE) |
| `Number_of_Arms` | Total number of study arms |
| `Shared_Control_Group` | Whether control group is shared across comparisons |
| `Shared_Intervention_Group` | Whether intervention group is shared |
| `Intervention_Group_ID` | Intervention group identifier |
| `Intervention_Group_ID_Standardized` | Standardized intervention group ID |
| `Total_Comparisons` | Total comparisons from this article |

### Risk of Bias (RoB 2 Tool)

| Variable | Description | Values |
|----------|-------------|--------|
| `RoB2_01_Randomization_Process` | Bias from randomization process | Low, Some Concerns, High |
| `RoB2_02_Deviations_From_Intended_Interventions` | Bias due to deviations from intended interventions | Low, Some Concerns, High |
| `RoB2_03_Missing_Outcome_Data` | Bias due to missing outcome data | Low, Some Concerns, High |
| `RoB2_04_Measurement_Of_Outcome` | Bias in measurement of outcome | Low, Some Concerns, High |
| `RoB2_05_Selection_Of_Reported_Result` | Bias in selection of reported result | Low, Some Concerns, High |
| `Overall_Risk_Of_Bias` | Overall risk of bias judgment | Low, Some Concerns, High |
| `High_RoB_Flag` | Flagged as high risk of bias |

### Data Provenance

| Variable | Description |
|----------|-------------|
| `Data_Type` | Type of data entry |
| `Data_Source` | Where data was obtained (text, table, figure, supplement) |
| `Data_Extraction_Method` | How data was extracted |
| `Morris_Method_Required` | Whether Morris method was needed |
| `Control_Original_Variance_Type` | Original variance type for control |
| `Intervention_Original_Variance_Type` | Original variance type for intervention |
| `Pre_Registration_Status` | Whether study was pre-registered |
| `Open_Data` | Whether data is openly available |

### Sensitivity Analysis Flags

| Variable | Description |
|----------|-------------|
| `any_sensitivity_flag` | Any sensitivity concern present |
| `sensitivity_age_violation` | Age outside inclusion criteria |
| `sensitivity_intervention_characteristics` | Atypical intervention |
| `sensitivity_statistical_issues` | Statistical concerns |
| `sensitivity_data_extraction` | Data extraction uncertainty |
| `Other_Sensitivity_Notes` | Additional sensitivity notes |
