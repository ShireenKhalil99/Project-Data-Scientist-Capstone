# Project-Data-Scientist-Capstone

### Table of Contents
1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [Files Description](#files)
4. [Key Steps in the Workflow](#Workflow)
5. [Result](#Result)
6. [Blog](#Blog)
7. [Conclusion](#Conclusion)
8. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>
The following libraries and installations were utilized in this project:
- [Python.3.13](https://www.python.org/downloads/)
- [Java.8](https://www.oracle.com/java/technologies/downloads/#java8-windows)
- [iPython Notebook](https://ipython.org/notebook.html)
- [PySpark](https://pypi.org/project/pyspark/)

   * **pyspark.sql**: DataFrame manipulation and SQL functions.
   * **pyspark.ml**: Machine learning pipelines and evaluation.

- [Pandas](http://pandas.pydata.org/)
- [seaborn](https://seaborn.pydata.org/)
- [ matplotlib](http://matplotlib.org/)
- [datetime](https://pypi.org/project/python-dateutil/)

## Project Motivation<a name="motivation"></a>
In today's competitive landscape, businesses must focus not only on acquiring new customers but also on retaining existing ones. Customer churn—the rate at which customers stop doing business with an entity—represents a critical challenge, especially in subscription-based services like Sparkify, a music streaming platform. High churn rates directly impact revenue, profitability, and growth potential.
The goal of this project is to address this challenge by leveraging data-driven insights to predict user churn. By identifying users at risk of leaving, Sparkify can proactively implement strategies such as personalized marketing, targeted retention offers, and improved user experiences. With effective churn prediction, Sparkify can improve customer satisfaction, enhance loyalty, and secure long-term revenue.

## Files Description<a name="files"></a>
- **Sparkify.ipynb**: Jupyter notebook containing the entire workflow, including data preprocessing, feature engineering, exploratory data analysis (EDA), and model training.
- **README.md**: This file, providing an overview of the project.
- **mini_sparkify_event_data.json**: Subset of the Sparkify dataset used for analysis.

  ## Key Steps in the Workflow<a name="Workflow"></a>
  **1. Data Cleaning**
     - Removed invalid or missing entries (e.g., rows with null userId or sessionId).
     - Filtered out users with empty userId.

  **2. Exploratory Data Analysis (EDA)**
      - Defined churn based on the Cancellation Confirmation page.
      - Visualized behavior differences between churned and non-churned users, such as subscription levels and page usage.

  **3. Feature Engineering**
      - A total of 8 features were engineered to train the machine learning models:
         * Number of Days Since Registration: Calculated from the registration date and the last activity timestamp.
         * Session Time Statistics: Average, minimum, and maximum session durations.
         * Average Songs Per Session: Average number of songs played in a session.
         * Number of Sessions: Count of unique sessions per user.
         * Gender: Encoded as binary (0 for Male, 1 for Female).
         * Subscription Level: Current subscription level (Free or Paid).
         * Page View Frequency: Frequency of interactions with specific pages (e.g., NextSong, Add to Playlist).
         * Unique Artists Count: Number of unique artists a user listened to.

   **4. Modeling**
    - Five machine learning models were trained and evaluated:
      * Logistic Regression
      * Random Forest
      * Gradient Boosted Trees
      * Decision Tree
      * Naive Bayes

## Result <a name="Result"></a>

<img width="529" alt="image" src="https://github.com/user-attachments/assets/6c511d6c-823a-43d4-bafb-15e9c6ca3746" />


- The **Logistic Regression** model achieved the highest F1 Score on both the validation and test datasets, making it the best-performing model for this problem.
- The analysis highlights clear differences in user behavior between churned and non-churned users. The Logistic Regression model effectively captures these differences, providing a reliable tool for churn prediction. This model can help Sparkify prioritize user retention efforts.

## Blog <a name="Blog"></a>
- For more details, kindly find my blog
  (https://shorturl.at/SbjMU)

## Conclusion <a name="Conclusion"></a>
This project demonstrates how data science can transform raw data into actionable insights. By identifying and predicting user churn, Sparkify can take proactive measures to retain its users, ensuring sustained growth and profitability. The techniques and findings from this project apply to a wide range of industries facing similar retention challenges.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>
  This project is part of the Udacity Data Scientist Nanodegree (https://learn.udacity.com/). The dataset and project outline were provided by Udacity.
