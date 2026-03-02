## Descriptive statistics

***Descriptive statistics*** summarizes qualities of a group (of people or things) numerically and visually.

Visual summaries uses graphical representations such as:

- Histogram
- Bar chart
- Box plot

![](./assets/data-viz-examples.png)

Example: In Snow's case, the data is the location of the cholera deaths. The frequency is the number of deaths in each location. The measures of central tendency are the location of the most deaths. The measures of dispersion are the range of the locations of the deaths.

## Inferential Statistics

***Inferential Statistics*** goes beyond description and into:

1. making informed guess about a group of people / items
2. verify claims through data; e.g., coffee and sleep

<img src="https://datatab.net/assets/tutorial/Descriptive_statistics_and_inferential_statistics.png">

Source: Datatab.

# Data Analysis

> **Data analysis** is the process of inspecting, cleansing, transforming, and modeling data with the goal of discovering useful information, informing conclusions, and supporting decision-making.

Two approaches to data analysis:

## A. Top-Down (Confirmatory - CDA)

Where we start with a question and use data to answer it.

Example Hypothesis: "people are addicted to smart phones". Let's see if the data supports this.

## B. Bottom-Up (Exploratory - EDA)

We start with the data and try to find something interesting.

Example Data: "people watching videos on our platform". Let's find out what piques their interest the most".

## The 4 Types of Data Analytics

See [Data Analytics](https://www.coursera.org/articles/data-analytics) (a more general term than: Data Analysis).

1. **Descriptive Analytics** (What happened?):
   - This is the foundation of business reporting. It uses historical data to summarize performance.
   - Example: A retail monthly sales report showing which regions met their quotas.

2. **Diagnostic Analytics** (Why did it happen?):
   - This involves "drilling down" into the data to find dependencies and causes.
   - Example: Investigating why sales dropped in May and discovering it was due to a specific supply chain bottleneck.

3. [**Predictive Analytics**](https://cloud.google.com/learn/what-is-predictive-analytics) (What will happen?):
   - This uses statistical models and machine learning to forecast future trends.
   - Example: A bank estimating the likelihood of a customer defaulting on a loan based on their credit history.

4. **Prescriptive Analytics** (How can we make it happen?):
   - The most advanced stage, where the analysis recommends specific actions to achieve an optimal outcome.
   - Example: An airline's pricing algorithm automatically adjusting ticket costs in real-time based on demand and weather patterns.

## Communication Types

### 1. Reporting

Reporting is the systematic tracking and formatting of data to show what is happening in the business, usually on a recurring basis.

* **What it involves:** Building dashboards or automated reports that track Key Performance Indicators (KPIs) like daily active users or monthly recurring revenue.
* **Why it matters:** It provides business stakeholders with a reliable, factual baseline of the company's health and historical performance.

### 2. Business Insights

This is the ultimate "so what?" of data science. It is the ability to translate data findings into actionable, strategic recommendations.

* **What it involves:** Understanding the company's business model, recognizing how data impacts the bottom line, and recommending specific actions (e.g., "Because user retention drops on day 3, we should send a targeted discount email on day 2").
* **Why it matters:** Data science is an investment. Business insights ensure that the investment actually generates value by guiding smarter decision-making.

## Communication Skills and Tools

### 1. Data Visualization

This is the visual representation of data. It is the bridge between complex numbers and human cognition.

* **What it involves:** Creating charts, graphs, and maps using tools like Tableau, Power BI, or Python libraries (matplotlib, seaborn, Plotly).
* **Why it matters:** The human brain processes visual information much faster than spreadsheets. Good visualization makes trends, outliers, and patterns immediately obvious.

### 2. Storytelling

Data storytelling is the art of crafting a narrative around data to guide the audience to a specific conclusion.

* **What it involves:** Combining data, visualizations, and narrative. It means knowing your audience, setting the context, highlighting the conflict or opportunity, and presenting a logical flow.
* **Why it matters:** Stakeholders rarely care about the technical details of a model. Storytelling translates complex analytical work into a compelling narrative that holds people's attention and persuades them.

# Key Steps in Data Analytics

### 3.3 Modeling

1. Make **inference** about population from sample
2. **Quantify relationships** (regression)
3. **Hypothesis testing**

## 1. Data Wrangling

### 1.1 Data Loading

Gather relevant data from sources:

1. Files (csv, excel, txt, json, xml, pdf, etc.)
2. Surveys (Google Forms, SurveyMonkey)
3. Web Scraping (BeautifulSoup, Scrapy, Selenium)
4. APIs (Twitter, Facebook, Google Maps, etc.)
5. Databases (SQL, NoSQL)

### 1.2 Data Cleaning

Prepare data for analysis by:

1. Select relevant columns
2. Impute missing values (or flag them as such)
    - Mean, Median, Mode
    - Forward fill, Backward fill
    - Interpolation
3. Remove duplicates
4. Correct errors (invalid values)
5. Remove irrelevant and redundant features
6. Column names' normalization
7. Value formats:
    1. Convert data types (e.g., `str -> datetime`)
    2. inconsistencies (e.g., `Female` and `F` both present in `gender` column)
    3. One format for dates, phone numbers, etc.

### 2.1 Scaling & Outlier Treatment

1. Scale the data:
    1. [**Normalize**](../techniques/02_transformation/normalize.ipynb)
        - Log Transformation
    2. [**Standardize**](../techniques/02_transformation/feature_scaling.ipynb)
        - Z-score
        - Min-max Scaling
        - Robust Scaling
2. [**Handle Outliers**](./L05_outliers.ipynb)
    - Z-score method
    - IQR method
    - 95th percentile
    - 99th percentile
    - Domain knowledge
3. Handle data imbalance
4. Encode categorical variables (e.g., one-hot encoding)

### 2.2 [Feature Engineering](../techniques/02_transformation/feature_engineering.ipynb)

Based on domain knowledge and questions to be answered:

1. Create new variables
    1. `age` from `date_of_birth`
    2. `BMI` from `weight` and `height`
    3. `season` from `date`
2. *Data Enrichment* - Add new data from external sources
    1. Geocoding (convert address to latitude and longitude using **Google Maps API**)
    2. Sentiment analysis (analyze text data using **OpenAI API**)
3. *Binning*
    1. `age_group` from `age`
    2. `income_group` from `income`
    3. `weight_category` from `weight`
4. Handle date-time variables
    1. Extract year, month, day, day of week, etc.
    2. Time since last purchase
    3. Time since first visit
5. Aggregate data
    1. `total_sales` from `sales` table
    2. `orders_count` from `orders` table
    3. `maximum_amount` from `transactions` table

### 2.3 [Feature Selection](../techniques/02_transformation/feature_selection.ipynb)

1. Select Features
    1. Correlation Coefficient
    2. Mutual information

### 3.1 Uni-variate Analysis

Understand the distribution of each variable.

1. *Descriptive Statistics*
    - Measure of central tendency (mean, median, mode)
    - Dispersion (range, variance, standard deviation)
    - Shape (skewness, kurtosis).
2. *Visualizations*
    - Histogram
    - Boxplot
    - Density plot
    - Violin plot
    - Bar plot
    - Pie chart
    - Frequency table
    - Word cloud

### 3.2 Multi-variate Analysis

Understand the relationship between multiple variables.

1. *Descriptive Statistics*
   - Covariance
   - Correlation
2. *Visualizations*
   - Scatter plot
   - Line plot
   - Heatmap
   - Pairplot
   - Boxplot
   - Violin plot
   - Bar plot
   - Stacked bar plot
   - Grouped bar plot

# Python Packages for Data Analysis

Python tools for data science are built on top of the following fundamental packages/libraries:

- **NumPy**: The fundamental **package** for scientific computing with Python.
- **SciPy**: Fundamental **algorithms** for scientific computing in Python.
- **Matplotlib** is a comprehensive library for creating static, animated, and interactive **visualizations** in Python.
Such Python libraries use **C** underneath to achieve high performance, yet provides it in a simple Pythonic Interface / API. As shown in the image below (for NumPy):

![Numpy Languages](../assets/numpy-languages.png)
We will use the following libraries in this course:

1. **Pandas**: for data wrangling and analysis.
2. **Seaborn**: for data visualization.
3. **statsmodels**: for statistical modeling and inference.
