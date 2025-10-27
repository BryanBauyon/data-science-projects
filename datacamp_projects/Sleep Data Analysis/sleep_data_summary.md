# 💤 DataCamp Project – *Sleep Data Analysis: Exploring Occupational and Health Factors Affecting Sleep*

## 🔗 Public Notebook  
[Open on DataCamp →](https://www.datacamp.com/datalab/w/abda49c7-609d-45ab-9843-8344cb7ff806/edit)

---

## 🏆 Overview  
This project explores how **occupation** and **BMI category** influence sleep duration, quality, and disorders such as insomnia.  
The analysis emphasizes **data cleaning**, **grouped summary statistics**, and **logical interpretation** — without relying on graphical visualization.

---

## 🧹 Data Cleaning  
- **Duplicate removal:** Ensured accurate group statistics using  
  `sleep_data = sleep_data.drop_duplicates()`  
- Final dataset: **374 records × 13 columns**, covering demographics, health metrics, and lifestyle factors:
  - `Age`, `Gender`, `Occupation`, `Sleep Duration`, `Quality of Sleep`, `BMI Category`, `Sleep Disorder`, etc.

---

## 🧩 Part 1: Sleep Duration by Occupation  

Calculated grouped summary statistics:

| Occupation            | Count | Min | Max | Mean |
|-----------------------|-------|-----|-----|------|
| Sales Representative  | 2     | 5.9 | 5.9 | 5.90 |
| Scientist             | 4     | 5.8 | 6.2 | 6.00 |
| Salesperson           | 32    | 6.3 | 6.5 | 6.40 |
| Teacher               | 40    | 6.3 | 7.2 | 6.69 |
| Software Engineer     | 4     | 5.9 | 7.5 | 6.75 |
| Manager               | 1     | 6.9 | 6.9 | 6.90 |
| Doctor                | 71    | 6.0 | 8.2 | 6.97 |
| Nurse                 | 73    | 5.9 | 8.2 | 7.06 |
| Accountant            | 37    | 6.5 | 8.0 | 7.11 |
| Lawyer                | 47    | 6.9 | 7.9 | 7.41 |
| Engineer              | 63    | 6.5 | 8.5 | 7.99 |

**Finding:**  
> Sales Representatives have the lowest average sleep duration — **5.9 hours per night**.

---

## 🧩 Part 2: Sleep Quality by Occupation  

Calculated similar grouped statistics for **sleep quality scores** (1–10 scale):

| Occupation            | Count | Min | Max | Mean |
|-----------------------|-------|-----|-----|------|
| Sales Representative  | 2     | 4 | 4 | 4.00 |
| Scientist             | 4     | 4 | 6 | 5.00 |
| Salesperson           | 32    | 6 | 6 | 6.00 |
| Software Engineer     | 4     | 4 | 8 | 6.50 |
| Doctor                | 71    | 6 | 9 | 6.65 |
| Teacher               | 40    | 5 | 8 | 6.98 |
| Manager               | 1     | 7 | 7 | 7.00 |
| Nurse                 | 73    | 5 | 9 | 7.37 |
| Accountant             | 37   | 7 | 9 | 7.89 |
| Lawyer                 | 47   | 7 | 8 | 7.89 |
| Engineer               | 63   | 5 | 9 | 8.41 |

**Finding:**  
> Sales Representatives also have the **lowest sleep quality**, scoring only **4.0** on average.

**Cross-check:**  
The same occupation (Sales Representative) had both the lowest **sleep duration** and **sleep quality**.  
`The occupation with the lowest sleep duration also have the lowest sleep quality: True`

---

## 🩺 Part 3: BMI Category and Insomnia Ratios  

Counted individuals by **BMI Category**, then compared how many within each category had **Insomnia**.

**Total BMI counts:**

| BMI Category | Count |
|--------------|--------|
| Normal       | 216 |
| Overweight   | 148 |
| Obese        | 10  |

**Individuals with Insomnia:**

| BMI Category | Count |
|--------------|--------|
| Overweight   | 64 |
| Normal       | 9 |
| Obese        | 4 |

Computed ratios of Insomnia cases within each BMI category:

`{'Normal': 0.04, 'Overweight': 0.43, 'Obese': 0.4}`

**Interpretation:**
- Only **4%** of people with a **Normal BMI** reported Insomnia.  
- Around **43% of Overweight** and **40% of Obese** individuals reported Insomnia.  
- Indicates a clear association between **higher BMI and increased Insomnia prevalence**.

---

## 💡 Insights & Learnings  

- **Occupational effects:** Some professions (like Sales) correlate with shorter and poorer sleep, likely due to irregular schedules or stress.  
- **Health relationship:** Increased BMI is strongly associated with Insomnia, highlighting the connection between weight management and sleep health.  
- **Analytical techniques:** Effective use of pandas for grouped summaries, conditional filtering, and ratio calculations — without the need for visual output.  
- **Clean data = clear insights:** Simple cleaning (like removing duplicates) ensured accurate, reproducible results.

---

## 🏁 Summary  
This project demonstrates a clean, structured approach to **data cleaning and descriptive analysis** using Python and pandas.  
By focusing on occupations, BMI, and sleep disorders, the analysis reveals that:
- **Sales Representatives** experience the **least sleep** (5.9 hours) and **worst quality** (score of 4.0).  
- **Overweight and Obese** individuals are **10× more likely** to experience Insomnia than those with normal BMI.  

Even without graphs, the notebook clearly shows how **data preparation and logical reasoning** can produce meaningful health insights.
