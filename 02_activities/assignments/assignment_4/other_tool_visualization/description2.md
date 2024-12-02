# Assignment 4: Data Visualization - another tool

## 1. What software did you use to create your data visualization?
The visualization was created using **SAS Studio** with the **PROC SGPANEL** and **PROC SGPLOT** procedures. These tools provide robust options for creating professional and informative visualizations.

---

## 2. Who is your intended audience?
The intended audience includes:
- **Public health researchers** and **data analysts**: To analyze trends in vaccination and hospitalization.
- **Policymakers**: To inform decisions on vaccination policies and public health measures.
- **Healthcare industry decision-makers**: To assess ICU and non-ICU hospitalization trends and their relationship with vaccination.

---

## 3. What information or message are you trying to convey with your visualization?
The key message of the visualization is:
- **ICU hospitalizations** have a higher proportion of unvaccinated individuals.
- **Non-ICU hospitalizations** are dominated by fully vaccinated individuals.
- Trends in hospitalization vary significantly based on vaccination status (unvaccinated, partially vaccinated, fully vaccinated).

---

## 4. What design principles did you consider and how were they applied?

### Substantive Principles
- Ensured the visualization clearly displayed **ICU** and **non-ICU hospitalization trends**.
- Used faceting to separate ICU and non-ICU data for clarity.

### Perceptual Principles
- **Stacked bar charts** were used to represent hospitalization proportions by vaccination status.
- Distinct colors were applied to differentiate vaccination groups (e.g., unvaccinated, partially vaccinated, fully vaccinated).

### Aesthetic Principles
- Facets for ICU and non-ICU hospitalizations were neatly arranged for comparison.
- The title and legends were intuitively designed to ensure readability and ease of understanding.

---

## 5. How did you ensure reproducibility, and what is the impact of non-reproducibility?

### Reproducibility
- The visualization is scripted in **SAS Studio**, allowing others to recreate the chart with the same dataset and code.
- Detailed documentation and clear scripts ensure consistent results.

### Impact of Non-Reproducibility
- Without reproducibility, the credibility of the results could be questioned.
- Outputs may vary in different environments, leading to misinterpretation or inconsistencies.

---

## 6. How did you ensure accessibility?
- **Faceting** was used to separate ICU and non-ICU hospitalizations, making it easier for audiences to interpret the data.
- High-contrast legend colors and readable text ensured vaccination statuses were easily distinguishable.
- A clean and simple design helped convey insights effectively.

---

## 7. Who might be impacted by your visualization?

### Direct Impact
- **Healthcare policymakers**: Can use the chart to understand the vaccination impact on hospitalization trends.
- **Public health decision-makers**: Can assess data to optimize vaccination strategies.

### Indirect Impact
- **General public**: Can see how vaccination reduces ICU admission risks, encouraging vaccine uptake.
- **Advocacy groups**: Can utilize the visualization for targeted vaccine promotion campaigns.

---

## 8. How did you select features to include or exclude?

### Included Features
- **Date**: To show trends over time.
- **Group**: Vaccination status (unvaccinated, partially vaccinated, fully vaccinated).
- **Type**: ICU or non-ICU hospitalization.
- **Count**: Total number of hospitalizations.

### Excluded Features
- **Irrelevant columns**: Such as IDs or unrelated fields, which were excluded to maintain focus and clarity.

---

## 9. What ‘underwater labour’ contributed to your final visualization product?

### Data Cleaning and Transformation
- Reshaped the data from wide to long format for compatibility with visualization tools.
- Checked for and resolved missing values or inconsistencies.

### Writing and Debugging SAS Scripts
- Developed and refined SAS scripts to ensure the visualization accurately reflected the data.

### Iteration and Refinement
- Adjusted colors, layout, and annotations iteratively to enhance clarity and impact.
- Tested various chart configurations to optimize the effectiveness of the final product.
