# Assignment 4: Data Visualization - using python

## 1. What software did you use to create your data visualization?
I used Python's **matplotlib** library to create the data visualizations. 

---

## 2. Who is your intended audience?
The intended audience includes:
- **General public**: To improve understanding of vaccination benefits.
- **Healthcare policymakers**: To guide vaccination campaigns.
- **Medical researchers**: To explore the relationship between vaccination and COVID-19 severity.

---

## 3. What information or message are you trying to convey with your visualization?
The key message is:
- **Unvaccinated individuals are at a higher risk of ICU admission.**
- **Vaccination significantly reduces the likelihood of severe illness, lowering ICU admissions.**

---

## 4. What design principles did you consider and how were they applied?

### Substantive
- Ensured accuracy by focusing on ICU and non-ICU hospitalization proportions.
- Chose metrics directly tied to hospitalization severity.

### Perceptual
- **Colors**: Blue (unvaccinated), orange (partially vaccinated), and green (fully vaccinated) were chosen for easy distinction.
- **Annotations**: Key insights, such as ICU admission rates, were emphasized.

### Aesthetic
- A **stacked bar chart** was used for clarity and effective layering.
- Neat arrangement avoided clutter; font sizes were optimized for readability.
- The legend was placed in the **top-right corner** to enhance usability.

---

## 5. How did you ensure reproducibility, and what is the impact of non-reproducibility?

### Reproducibility
- The visualization is fully reproducible through Python code, including data loading, cleaning, and visualization.
- Anyone with the dataset and code can replicate the chart.

### Impact of Non-Reproducibility
- Non-reproducible processes reduce the visualization’s credibility as viewers cannot verify the data's accuracy or completeness.

---

## 6. How did you ensure accessibility?
- **Clear color contrasts** and a simple chart design enhanced accessibility for diverse audiences.
- **Annotations** clarified insights for viewers from varied backgrounds.
- **Readable font sizes** ensured clarity, avoiding overly small text.

---

## 7. Who might be impacted by your visualization?

### Direct Impact
- **Healthcare policymakers**: To optimize vaccination campaigns.
  
### Indirect Impact
- **General public**: To motivate vaccine uptake by illustrating the benefits of vaccination.

---

## 8. How did you select features from the dataset to include or exclude?

### Included Features
- Data directly tied to hospitalization severity: **ICU and non-ICU admissions.**
- Three key vaccination statuses: **unvaccinated, partially vaccinated, and fully vaccinated.**

### Excluded Features
- **Temporal data**: Dates were excluded as they were irrelevant to the message.
- **Other irrelevant columns** (e.g., `_id`) were omitted.

---

## 9. What ‘underwater labour’ contributed to your final visualization?

### Data Preparation
- Cleaning and preprocessing: Addressed missing values, converted data types, and calculated totals for ICU and non-ICU admissions.
- Normalization: Converted raw numbers into proportions for better interpretability.

### Design Optimization
- Selected appropriate colors, adjusted annotation placement, and arranged titles and legends for clarity.

### Iterative Debugging
- Refined the chart to ensure it was visually appealing and conveyed the intended message effectively.
