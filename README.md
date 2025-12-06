# Global Nutrition Transitions and Obesity Trends

## Project Overview

This comprehensive analysis examines how global dietary patterns and nutrition availability have evolved over time, and how these transitions relate to obesity trends among adults and children worldwide. The project integrates data from WHO Global Health Observatory and FAOSTAT to provide insights into nutrition-obesity relationships across different countries and demographics.

## 🎯 Research Objectives

### Primary Goal
To analyze the relationship between global dietary patterns, nutrition availability, and obesity trends across different populations and time periods.

### Key Research Questions

#### A. Trend-Based Analysis
- How have obesity rates changed globally over the last 20–30 years?
- Are adults and children following similar or different obesity patterns over time?
- Which regions/countries show the sharpest increase or decrease in obesity?

#### B. Nutrition & Diet Pattern Analysis
- How has per-capita food supply (kcal, fats, sugars, proteins) changed globally?
- Is increased calorie or sugar supply associated with higher obesity rates?
- Are there specific nutrition indicators that strongly predict obesity?

#### C. Demographic & Inequality Analysis
- Are obesity trends different across male vs female populations?
- How do children vs adults differ in obesity levels across countries?
- Do different age groups show varying risk levels?

#### D. Risk Factor Correlation Analysis
- Do high-income countries show different nutrition-obesity patterns compared to low-income countries?
- Which countries are outliers (e.g., high calories but low obesity)?
- Are there clusters of countries with similar dietary and obesity profiles?

#### E. Predictive Analysis
- Can we predict obesity rates from nutrition supply and demographic factors?
- Which factors contribute most to obesity (feature importance)?

## 📊 Data Sources

### WHO Global Health Observatory (API)
- **Coverage**: ~170 to 190+ countries
- **Time Range**: 1983–2024 (varies by indicator)
- **Key Indicators**:
  - Adult obesity prevalence (age-standardized)
  - Child & adolescent obesity (crude rates)
  - Under-5 overweight, wasting, and stunting prevalence
  - Demographic splits by sex and age groups
- **Status**: ✅ Successfully collected and analyzed

### FAOSTAT (FAO)
- **Indicators**:
  - National food supply (kcal, fat, sugar, protein availability)
  - Nutrition composition indicators
- **Coverage**: Limited to 3 overlapping country-year entries with WHO data
- **Status**: ⚠️ Collected but insufficient for robust analysis

### Kaggle Datasets
- Individual-level obesity prediction dataset (2111 entries, 17 features)
- Behavioral and demographic factors
- **Status**: ✅ Successfully analyzed with EDA completed

## 🔍 Key Findings

### 1. Global Obesity Trends (1990-2022)

**Consistent Upward Trajectory**
- Obesity rates show steady increases across all demographics
- 1990-1994: 10.70% → 12.03% (adult obesity)
- Driven by urbanization, dietary transitions, and globalization

**Sex-Based Patterns**
- **Adults**: Females consistently show higher obesity rates than males
- **Children**: Males show higher obesity rates than females
- Both patterns maintain parallel upward trends

### 2. Adult-Child Obesity Correlations

**Strong Positive Correlations (Most Countries)**
- Correlation range: 0.6 to 0.9
- Countries with >0.9 correlation: Afghanistan, Argentina, New Zealand, UK, Pakistan
- Indicates synchronized obesity trends across age groups

**Divergent Patterns (Exceptional Cases)**
- **Negative correlations**: Denmark (-0.25), Japan (-0.009), Kyrgyzstan (-0.45)
- **Low correlations**: Haiti (0.09), Spain (0.12), Ukraine (0.20)
- Suggest successful age-specific interventions or unique local factors

### 3. Nutrition-Obesity Relationships

**Critical Data Limitations**
- Only 3 overlapping country-year entries between FAOSTAT and WHO data
- Results not statistically significant or generalizable
- Counter-intuitive negative correlations likely due to small sample size

**Observed Patterns (Limited Reliability)**
- Protein intake: Strong negative correlation with obesity (-0.98 to -0.99)
- Energy/carbohydrates: Negative correlations (-0.72 to -0.87)
- Adult-child obesity: Strong positive correlation (0.99)

### 4. Individual-Level Obesity Analysis (EDA)

**Dataset Characteristics**
- 2111 individuals across 7 obesity categories
- 24 duplicate entries removed for data quality
- Complete data with no missing values

**Key Behavioral Findings**
- **Family history**: Strong predictor of obesity risk
- **High-caloric food consumption**: Significantly associated with higher obesity levels
- **Eating between meals**: 'Sometimes' and 'Frequently' linked to overweight/obesity
- **Transportation mode**: Walking/motorbike users tend toward lower weight categories

**Demographic Patterns**
- **Gender differences**: Females more prevalent in insufficient weight; males dominate severe obesity categories
- **Age trends**: Higher obesity levels associated with slightly older populations
- **Weight progression**: Clear increasing trend from insufficient weight to obesity Type III

### 5. Country Case Studies

**Japan: Child Obesity Prevention Success**
- Mandatory balanced school meals
- Compulsory daily physical education
- Child obesity remains among world's lowest

**Kyrgyzstan: Economic Impact**
- Economic hardship reducing adult obesity
- Slight increases in childhood overweight
- Migration effects on survey data

## 📁 Project Structure

```
Nutrition_and_obesity_trends/
├── assets/                          # Generated visualizations (20+ plots)
│   ├── Global trend plots
│   ├── Correlation heatmaps
│   ├── Sex-wise analysis charts
│   └── Individual-level EDA plots
├── Inferences/                      # Analysis reports and findings
│   ├── adult_child_obesity_correlation_analysis.md
│   ├── food_supply_analysis.md
│   ├── global_obesity_analysis.md
│   ├── nutrition_vs_obesity_analysis.md
│   ├── obesity_trends.md           # Individual-level EDA findings
│   └── sex_wise_obesity_trends.md
├── Notebook/                        # Jupyter notebooks for analysis
│   ├── A.setup_and_import.ipynb   # Environment setup
│   ├── B.Data_Cleaning.ipynb      # WHO/FAOSTAT data processing
│   ├── C.Analyse.ipynb            # Statistical analysis
│   └── D.EDA.ipynb                # Individual-level exploration
├── Plots/                          # Plot generation scripts
├── Data_Collection.md              # Data sources documentation
└── README.md                       # Project documentation
```

## 🛠️ Technical Implementation

### Data Processing Pipeline
1. **Data Collection**: WHO API integration, FAOSTAT processing, Kaggle datasets
2. **Data Cleaning**: Country standardization, missing value handling, temporal alignment
3. **Integration**: Merging datasets by country-year combinations
4. **Analysis**: Correlation analysis, trend analysis, visualization generation

### Key Technologies
- **Python**: Primary analysis language
- **Pandas**: Data manipulation and analysis
- **Matplotlib/Seaborn**: Visualization
- **Scikit-learn**: Machine learning and statistical analysis
- **WHO API**: Real-time health data access
- **Jupyter Notebooks**: Interactive analysis environment

## 📈 Visualizations Generated (20+ Charts)

### Global Trends
- Global mean obesity rates (1990-2022)
- Sex-wise obesity trends for adults and children
- Age group analysis for different obesity indicators
- Under-5 malnutrition trends

### Correlation Analysis
- Adult-child obesity correlation heatmaps
- Country-specific correlation patterns
- Nutrition vs. obesity scatter plots (limited data)
- Sugar availability correlation matrices

### Individual-Level Analysis
- Obesity distribution by categories
- Gender-based obesity patterns
- Age, height, weight distributions by obesity level
- Behavioral factor correlations

### Country Comparisons
- Top 20 countries with largest adult-child obesity disparities
- Regional obesity pattern analysis
- Outlier country identification

## ⚠️ Limitations and Considerations

### Data Quality Issues
- **Limited FAOSTAT coverage**: Only 3 overlapping entries with WHO data
- **Temporal gaps**: Inconsistent data availability across years
- **Geographic bias**: Better coverage for developed countries
- **Measurement variations**: Different methodologies across datasets

### Statistical Limitations
- **Small sample sizes**: Insufficient for robust statistical inference
- **Correlation vs. causation**: Cannot establish causal relationships
- **Missing confounders**: Limited socioeconomic and policy variables

### Methodological Constraints
- **Cross-sectional analysis**: Limited longitudinal tracking
- **Aggregated data**: Country-level analysis masks within-country variation
- **Data integration challenges**: Inconsistent country coding and temporal alignment

## 🔮 Future Directions

### Data Enhancement
- Expand FAOSTAT data collection for better temporal coverage
- Integrate additional nutrition databases
- Include socioeconomic and policy variables
- Develop standardized country-year matching protocols

### Analytical Improvements
- Implement longitudinal analysis methods
- Develop predictive models with adequate sample sizes
- Conduct sub-national analysis where data permits
- Integrate machine learning approaches for pattern recognition

### Policy Applications
- Develop country-specific intervention recommendations
- Create early warning systems for obesity trends
- Design targeted nutrition policies based on correlation patterns
- Establish monitoring frameworks for nutrition-obesity relationships

## 📚 Key Insights for Public Health

### Policy Implications
1. **System-wide approaches** needed for countries with high adult-child obesity correlations
2. **Age-specific strategies** valuable for countries with divergent patterns
3. **School-based interventions** can effectively decouple child obesity from adult trends
4. **Economic factors** significantly influence obesity patterns in lower-income countries

### Research Priorities
1. **Data Integration**: Expand FAOSTAT-WHO overlap for robust nutrition-obesity analysis
2. **Individual Prediction**: Develop machine learning models using behavioral factors
3. **Policy Mechanisms**: Understand successful child obesity prevention strategies (Japan, Denmark)
4. **Economic Factors**: Investigate how economic transitions affect obesity patterns
5. **Longitudinal Studies**: Track individual and country-level changes over time

## 📊 Analysis Status

### ✅ Completed Analyses
- [x] Global obesity trends (1990-2022)
- [x] Adult-child obesity correlations
- [x] Sex-wise obesity patterns
- [x] Individual-level behavioral analysis
- [x] Country case studies
- [x] Data visualization suite (20+ charts)

### ⚠️ Limited/Inconclusive
- [x] Nutrition-obesity correlations (insufficient data overlap)
- [x] Predictive modeling (requires expanded dataset)

### 🔄 Future Work
- [ ] Machine learning prediction models
- [ ] Expanded nutrition data collection
- [ ] Longitudinal trend analysis
- [ ] Policy intervention assessment

## 🤝 Contributing

This project provides a comprehensive foundation for understanding global nutrition-obesity relationships. Future contributions should focus on:
- **Data expansion**: Acquiring more comprehensive nutrition datasets
- **Model development**: Building predictive models for obesity risk
- **Policy analysis**: Evaluating intervention effectiveness
- **Visualization enhancement**: Interactive dashboards and tools

## 📄 License

This project is developed for research and educational purposes. Data sources maintain their respective licenses and usage terms.

## 🎯 Key Deliverables

- **6 comprehensive analysis reports** in `Inferences/` directory
- **20+ visualizations** documenting trends and patterns
- **4 Jupyter notebooks** with reproducible analysis pipeline
- **Cleaned datasets** ready for further research
- **Policy recommendations** based on correlation findings

---

*For detailed analysis results, please refer to the individual reports in the `Inferences/` directory and visualizations in the `assets/` folder.*