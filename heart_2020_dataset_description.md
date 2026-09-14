# Heart Disease 2020 Dataset — Description

## Overview

This dataset is drawn from the CDC's Behavioral Risk Factor Surveillance System (BRFSS), an annual health survey of over 400,000 U.S. adults. This cleaned version contains **319,795 respondents** and **18 columns** covering demographics, lifestyle habits, and health conditions, with the goal of studying factors associated with heart disease.

Binary (Yes/No or Male/Female) columns have been encoded numerically as `0`/`1`. Columns with more than two categories (AgeCategory, Race, Diabetic, GenHealth) have been left as text labels.

---

## Column Descriptions

| Column | Type | Description |
|---|---|---|
| **HeartDisease** | Binary (0/1) | Target variable. Whether the respondent has ever been told they had coronary heart disease (CHD) or myocardial infarction (MI). `1` = Yes, `0` = No. |
| **BMI** | Numeric (float) | Body Mass Index, a measure of body fat based on height and weight. Ranges roughly from 12 to 95 in this dataset. |
| **Smoking** | Binary (0/1) | Whether the respondent has smoked at least 100 cigarettes in their entire life (≈5 packs). `1` = Yes, `0` = No. |
| **AlcoholDrinking** | Binary (0/1) | Whether the respondent is a heavy drinker (adult men having more than 14 drinks/week, adult women more than 7 drinks/week). `1` = Yes, `0` = No. |
| **Stroke** | Binary (0/1) | Whether the respondent has ever been told they had a stroke. `1` = Yes, `0` = No. |
| **PhysicalHealth** | Numeric (int, 0–30) | Number of days in the past 30 days the respondent's physical health (illness/injury) was "not good." |
| **MentalHealth** | Numeric (int, 0–30) | Number of days in the past 30 days the respondent's mental health was "not good" (stress, depression, emotional problems). |
| **DiffWalking** | Binary (0/1) | Whether the respondent has serious difficulty walking or climbing stairs. `1` = Yes, `0` = No. |
| **Sex** | Binary (0/1) | Respondent's biological sex. `0` = Female, `1` = Male. |
| **AgeCategory** | Categorical (text) | 13 age brackets, from `18-24` up to `80 or older`, in 5-year intervals. |
| **Race** | Categorical (text) | Self-reported race/ethnicity: White, Black, Asian, American Indian/Alaskan Native, Hispanic, or Other. |
| **Diabetic** | Categorical (text) | Diabetes status: `No`, `Yes`, `No, borderline diabetes`, or `Yes (during pregnancy)`. |
| **PhysicalActivity** | Binary (0/1) | Whether the respondent reported any physical activity/exercise outside of their regular job in the past 30 days. `1` = Yes, `0` = No. |
| **GenHealth** | Categorical (text) | Respondent's self-rated general health: `Excellent`, `Very good`, `Good`, `Fair`, or `Poor`. |
| **SleepTime** | Numeric (int, hours) | Average number of hours of sleep per 24-hour period. |
| **Asthma** | Binary (0/1) | Whether the respondent has ever been told they have asthma. `1` = Yes, `0` = No. |
| **KidneyDisease** | Binary (0/1) | Whether the respondent has ever been told they have kidney disease (excluding kidney stones, bladder infection, or incontinence). `1` = Yes, `0` = No. |
| **SkinCancer** | Binary (0/1) | Whether the respondent has ever been told they have skin cancer. `1` = Yes, `0` = No. |

---

## Notes

- **Target variable:** `HeartDisease` is typically used as the label for classification tasks predicting heart disease risk.
- **Class imbalance:** Heart disease datasets like this are usually heavily imbalanced (far more "No" than "Yes" cases), which should be accounted for during modeling (e.g., resampling, class weighting).
- **Encoding choice:** Only strictly two-category columns were converted to numeric 0/1 values. Multi-category columns (AgeCategory, Race, Diabetic, GenHealth) were intentionally left as text since they carry more than two levels and may need ordinal or one-hot encoding depending on the modeling approach.
