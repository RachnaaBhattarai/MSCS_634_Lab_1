# MSCS_634_Lab_1

**MSCS_634_Lab_1: Data Visualization, Preprocessing, and Statistical Analysis**

# Purpose of the Lab Work:
This lab assignment was conducted to explore the heart disease dataset (`heart.csv`) using Python within a Jupyter Notebook environment. The primary goals were to apply fundamental data analysis techniques, including data visualization for initial exploration, data preprocessing to clean and prepare the dataset, and statistical analysis to understand its underlying characteristics and relationships between variables. This process is crucial for gaining initial insights and preparing the data for more advanced machine learning tasks.

# Key Insights from Visualizations and Statistical Measures:

Age vs. Cholesterol Scatter Plot: The scatter plot of age versus cholesterol, colored by the presence of heart disease, revealed a tendency for cholesterol levels to be higher across all age groups for individuals with heart disease. While there isn't a strict linear correlation, the distribution suggests that higher cholesterol values might be a contributing factor or a consequence associated with heart disease in this dataset.

Heart Disease Prevalence by Sex Bar Chart: The bar chart comparing heart disease prevalence by sex indicated a higher number of male patients diagnosed with heart disease compared to female patients in this specific dataset. This observation warrants further investigation to understand potential gender-related factors influencing heart disease.

General Overview: The `.info()` output confirmed that the dataset contains 303 entries and 14 columns, with each column having a consistent number of non-null values, reinforcing the initial observation of no missing data. The `.describe()` output provided key statistical summaries for the numerical features, including count, mean, standard deviation, minimum, quartiles, and maximum values. This gave us an initial understanding of the central tendency and spread of these variables. For instance, the average age of patients is around 54, and the mean cholesterol level is approximately 246 mg/dl.

Correlation Analysis: The correlation matrix highlighted several interesting relationships. For example, there was a positive correlation between `cp` (chest pain type) and `target` (presence of heart disease), suggesting that certain types of chest pain might be more indicative of heart disease. Conversely, `thalach` (maximum heart rate achieved) showed a negative correlation with `target`, implying that a lower maximum heart rate might be associated with a higher likelihood of heart disease. `oldpeak` (ST depression induced by exercise) also showed a positive correlation with `target`.

Age Distribution Histogram: The histogram of patient ages showed a distribution skewed towards the older age groups, with a significant number of patients falling in the 50-65 age range.

Cholesterol Levels Box Plot: The box plot of cholesterol levels, separated by heart disease status, visually confirmed that the median cholesterol level appears higher for patients with heart disease, and also highlighted the presence of potential outliers in the cholesterol levels for both groups.

# Challenges Faced or Decisions Made During the Lab:

Handling Missing Values (Hypothetical): Although the dataset was initially reported as having no missing values, the lab instructions required demonstrating the process. The decision was made to show the `isnull().sum()` check before and after a hypothetical imputation (filling with the mean for 'chol'), even though no actual imputation was performed on this clean dataset. This demonstrated the code that would be used if missing values were present.

Outlier Detection and Management: Outliers were detected in the 'chol' column using the IQR method. While the outliers were identified, the decision to not remove them for the purpose of this initial exploratory analysis was made. Removing outliers can sometimes lead to loss of important information, and further investigation into the nature of these high cholesterol values might be warranted in a real-world scenario. The code for removal was included but commented out to highlight this decision.

Data Reduction: The 'restecg' column (resting electrocardiographic results) was hypothetically chosen as a less relevant feature for the sake of demonstrating data reduction. This was a subjective decision made to fulfill the lab requirement. In a real-world analysis, a more thorough feature importance analysis would be conducted before dropping any columns.

Data Scaling: Min-Max scaling was chosen to scale the 'age' and 'trestbps' columns. This method scales the data to a range between 0 and 1, which can be beneficial for certain machine learning algorithms. Z-score standardization was considered but Min-Max scaling was selected for this demonstration due to its straightforward interpretation of the scaled values within a defined range.

Data Discretization: The 'age' column was discretized into meaningful categorical bins ('Young Adult', 'Middle-Aged', 'Older Adult', 'Senior') to explore potential non-linear relationships between age groups and heart disease. The bin edges were chosen based on common age-related health categories.

# Key Insights from the Dataset.

The dataset comprises 303 patient records with 14 features, encompassing a mix of numerical (e.g., age, blood pressure, cholesterol) and categorical (e.g., sex, chest pain type) variables.
The absence of missing values simplifies the initial preprocessing steps.
The target variable ('target'), indicating the presence or absence of heart disease, appears to be relatively balanced, which is advantageous for training classification models as it reduces potential bias towards the majority class. The distribution shown in the pie chart confirmed a near 50/50 split.
The dataset provides a rich set of medical indicators that can be further analyzed to understand the factors contributing to heart disease.
