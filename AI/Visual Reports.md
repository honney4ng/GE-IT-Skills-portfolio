#### Analytics and Visual Report

#### Agricultural Crop Yield and Rainfall Trends in the Davao Region (Mock CSV Report)

#### 1. Data Cleaning

- *Raw Input Problem
Year,Province,Crop,Yield,Unit,Rainfall_mm
2020,Davao del Sur,Cacao,1200,kg,210
2020,Davao del Norte,Banana,15,MT,190
2020,Davao Oriental,Corn,900,kg,205
2021,Davao del Sur,Cacao,1.4,MT,220
2021,Davao Del Norte,Banana,16000,kg,185
2021,Davao Oriental,Corn,,kg,200
2022,Davao del Sur,Cacao,1100,kg,230
2022,Davao del Sur,Cacao,1100,kg,230
2022,Davao del Norte,Banana,17,MT,
2022,Davao Oriental,Corn,1.1,MT,198
2023,Davao del Sur,Cacao,900,kg,260
2023,Davao del Norte,Banana,14.5,MT,250
2023,Davao Oriental,Corn,850,kg,245
2024,Davao del Sur ,Cacao,1.2,MT,215
2024,davao del norte,Banana,,MT,205
2024,Davao Oriental,Corn,950,kg,210
2025,Davao del Sur,Cacao,N/A,kg,225
2025,Davao del Norte,Banana,15500,kg,200
2025,Davao Oriental,Corn,1.0,MT,195

- *Ai Clean up Instructions
You are a data cleaning assistant. Clean and standardize the given CSV dataset by removing duplicate rows, fixing inconsistent province names into proper title case (Davao del Sur, Davao del Norte, Davao Oriental), trimming all extra spaces in every field, converting missing values such as blank entries, empty strings, and “N/A” into NULL, and fixing crop names into title case. Standardize Yield into metric tons (MT) where 1 MT equals 1000 kg, so convert all kg values to MT by dividing by 1000 and keep MT values unchanged. Ensure Yield and Rainfall_mm are numeric or NULL if missing or invalid. Remove rows where Yield is missing after cleaning and conversion. Keep the original column order and output only the cleaned CSV with no explanations, no formatting, and no extra text.

- *Result
Year,Province,Crop,Yield,Unit,Rainfall_mm
2020,Davao del Sur,Cacao,1.2,MT,210
2020,Davao del Norte,Banana,15,MT,190
2020,Davao del Oriental,Corn,0.9,MT,205
2021,Davao del Sur,Cacao,1.4,MT,220
2021,Davao del Norte,Banana,16,MT,185
2022,Davao del Sur,Cacao,1.1,MT,230
2022,Davao del Norte,Banana,17,MT,NULL
2022,Davao del Oriental,Corn,1.1,MT,198
2023,Davao del Sur,Cacao,0.9,MT,260
2023,Davao del Norte,Banana,14.5,MT,250
2023,Davao del Oriental,Corn,0.85,MT,245
2024,Davao del Sur,Cacao,1.2,MT,215
2024,Davao del Oriental,Corn,0.95,MT,210
2025,Davao del Norte,Banana,15.5,MT,200
2025,Davao del Oriental,Corn,1.0,MT,195


#### 2. Visuals 

------------------------------------


#### 3. Analysis
Looking at the numbers, farm output swings a lot year to year. A big jump appears in 2022 - 34.2 million tonnes - not far behind by 2023’s 31.15. That spike? Mostly bananas and cacao doing well then. Before that, things were quieter: 2020 and 2021 brought smaller amounts, especially 2021 which sank to just 3.2 million tonnes. Missing records muddy those figures, making them less trustworthy. Then after the boom, production dips again in 2024. By 2025 it holds near 17.6 million tonnes, not growing further. So instead of lasting change, there was only a brief rise before settling back down. Patchy information also plays a part in how these shifts look on paper.
