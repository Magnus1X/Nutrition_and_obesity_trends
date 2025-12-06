## EDA Findings and Insights

### 1. Distribution of Obesity Levels (`NObeyesdad`)
- The dataset shows a relatively even distribution across different obesity levels, with 'Obesity_Type_I' being the most frequent, followed by 'Obesity_Type_III', 'Obesity_Type_II', 'Overweight_Level_I', 'Overweight_Level_II', 'Normal_Weight', and 'Insufficient_Weight'.
- All categories are well-represented, which is good for training predictive models.

### 2. Obesity Levels by Gender (`Gender` vs. `NObeyesdad`)
- **Insufficient_Weight** is more prevalent among females.
- **Normal_Weight** shows a balanced distribution between genders.
- **Overweight_Level_I** and **Overweight_Level_II** are fairly balanced.
- **Obesity_Type_I** appears to have a higher count for females.
- **Obesity_Type_II** is predominantly male.
- **Obesity_Type_III** is overwhelmingly male.

### 3. Distribution of Numerical Features by Obesity Level (`Age`, `Height`, `Weight` vs. `NObeyesdad`)
- **Age**:
    - Generally, higher obesity levels (Obesity_Type_I, II, III) are associated with slightly older age distributions, though there's significant overlap across all levels.
    - `Insufficient_Weight` and `Normal_Weight` tend to have younger age distributions.
- **Height**:
    - There isn't a strong direct correlation between height and obesity level; height distributions are similar across most categories. However, `Obesity_Type_III` shows a slightly taller distribution, while `Insufficient_Weight` shows a slightly shorter distribution.
- **Weight**:
    - As expected, there's a clear increasing trend in weight as the obesity level progresses from `Insufficient_Weight` to `Obesity_Type_III`. This is a strong indicator.

### 4. Relationship with Other Categorical Variables
- **Family History with Overweight (`family_history_with_overweight`)**:
    - A strong positive correlation is observed: individuals with a family history of overweight are significantly more likely to fall into `Overweight` and `Obesity` categories.
- **Consumption of high caloric food (`FAVC`)**:
    - Individuals who frequently consume high caloric food ('yes') are more common in `Overweight` and `Obesity` categories.
- **Consumption of food between meals (`CAEC`)**:
    - 'Sometimes' and 'Frequently' consumption of food between meals is higher in `Overweight` and `Obesity` categories, particularly 'Sometimes'.
- **Smoking (`SMOKE`)**:
    - Smoking status does not show a very strong or distinct pattern across different obesity levels in this dataset.
- **Transportation (`MTRANS`)**:
    - 'Public_Transportation' is the most common mode across all obesity levels, but a higher proportion of individuals using 'Walking' or 'Motorbike' tend to be in lower weight categories (Insufficient/Normal Weight), while 'Automobile' usage is slightly more associated with higher obesity types.
### Data Analysis Key Findings
*   The initial dataset contained 2111 entries and 17 columns, with no missing values.
*   A total of 24 duplicate rows were identified and successfully removed, ensuring data uniqueness.
*   The 'NObeyesdad' column was successfully converted to an ordered categorical type, facilitating analysis based on obesity severity.
*   'Obesity\_Type\_I' was the most frequent obesity category, followed by 'Obesity\_Type\_III'.
*   **Gender Differences**: 'Insufficient\_Weight' was more prevalent among females, while 'Obesity\_Type\_II' and 'Obesity\_Type\_III' were predominantly observed in males.
*   **Age and Weight Trends**: Higher obesity levels were generally associated with slightly older age distributions. A clear and strong increasing trend in weight was observed as the obesity level progressed from 'Insufficient\_Weight' to 'Obesity\_Type\_III', as expected.
*   **Height Correlation**: No strong direct correlation was found between height and obesity level; however, 'Obesity\_Type\_III' individuals tended to be slightly taller, and 'Insufficient\_Weight' individuals slightly shorter.
*   **Behavioral and Genetic Factors**:
    *   A strong positive correlation exists between having a `family_history_with_overweight` and falling into higher overweight and obesity categories.
    *   Frequent consumption of high caloric food (`FAVC`) and eating between meals (`CAEC` - 'Sometimes'/'Frequently') were more common in overweight and obesity groups.
    *   Smoking status (`SMOKE`) did not show a distinct pattern related to obesity levels.
    *   Individuals using `Walking` or `Motorbike` for transportation tended to be in lower weight categories, whereas `Automobile` users were slightly more associated with higher obesity types.