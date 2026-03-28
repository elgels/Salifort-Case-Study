<h1>Salifort Employee Retention Analysis</h1>

<h2>Project Overview</h2>
<p>
This project analyzes employee data from <strong>Salifort Motors</strong> to identify factors associated with employee turnover and to build models that predict whether an employee is likely to leave the company.
</p>

<p>
Employee retention is an important issue for organizations because recruiting and training new employees is costly and time-consuming. By identifying the factors that contribute to employee attrition, the HR department can implement strategies to improve employee satisfaction and retention.
</p>

<p>
This project was completed as part of the <strong>Google Advanced Data Analytics Professional Certificate Capstone Project</strong>.
</p>

<h2>Business Problem</h2>
<p>
The HR department at Salifort Motors collected employee data but needed help answering the following question:
</p>

<blockquote>
<p><strong>What’s likely to make the employee leave the company?</strong></p>
</blockquote>

<p>The goal of the analysis was to:</p>
<ul>
  <li>Identify factors associated with employee turnover.</li>
  <li>Build predictive models to classify employees likely to leave.</li>
  <li>Provide data-driven recommendations to improve employee retention.</li>
</ul>

<h2>Dataset</h2>
<p>
The dataset contains approximately <strong>15,000 employee records</strong> and 10 variables describing employee satisfaction, workload, tenure, salary level, and department.
</p>

<p><strong>Key variables include:</strong></p>
<ul>
  <li><code>satisfaction_level</code> – employee reported job satisfaction</li>
  <li><code>last_evaluation</code> – performance evaluation score</li>
  <li><code>number_project</code> – number of projects assigned</li>
  <li><code>average_monthly_hours</code> – average hours worked per month</li>
  <li><code>time_spend_company</code> – employee tenure</li>
  <li><code>work_accident</code> – employee experienced an accident at work</li>
  <li><code>promotion_last_5years</code> – promotion status</li>
  <li><code>department</code> – department</li>
  <li><code>salary</code> – salary in U.S. dollars</li>
  <li><code>left</code> – target variable indicating whether the employee left or stayed</li>
</ul>

<h2>Methods</h2>
<p>The analysis followed a standard data science workflow:</p>

<h3>1. Data Exploration and Cleaning</h3>
<ul>
  <li>Inspected data types and summary statistics.</li>
  <li>Removed duplicate observations.</li>
  <li>Examined potential outliers.</li>
  <li>Renamed variables for clarity.</li>
</ul>

<h3>2. Exploratory Data Analysis</h3>
<p>Visualization techniques included:</p>
<ul>
  <li>Histograms for numeric variables.</li>
  <li>Bar plots for categorical variables.</li>
  <li>Boxplots comparing features with employee turnover.</li>
  <li>Correlation heatmaps.</li>
  <li>Pairplots for variable relationships.</li>
</ul>

<p>These visualizations helped identify patterns related to employee attrition.</p>

<h3>3. Feature Engineering</h3>
<ul>
  <li>One-hot encoding of categorical department variables.</li>
  <li>Ordinal encoding of salary levels.</li>
  <li>Removal of outliers for logistic regression modeling.</li>
</ul>

<h3>4. Predictive Modeling</h3>
<p>Three classification models were implemented:</p>
<ul>
  <li><strong>Logistic Regression</strong></li>
  <li><strong>Decision Tree</strong></li>
  <li><strong>Random Forest</strong></li>
</ul>

<p>
Hyperparameter tuning was performed using <code>GridSearchCV</code> with cross-validation.
</p>

<p>Models were evaluated using:</p>
<ul>
  <li>Accuracy</li>
  <li>Precision</li>
  <li>Recall</li>
  <li>F1-score</li>
  <li>ROC–AUC</li>
</ul>

<h2>Results</h2>
<p>
The <strong>Random Forest model</strong> produced the best predictive performance.
</p>

<h3>Model Performance</h3>
<table>
  <thead>
    <tr>
      <th>Metric</th>
      <th>Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Accuracy</td>
      <td>98.23%</td>
    </tr>
    <tr>
      <td>Precision</td>
      <td>98.41%</td>
    </tr>
    <tr>
      <td>Recall</td>
      <td>90.82%</td>
    </tr>
    <tr>
      <td>F1 Score</td>
      <td>94.46%</td>
    </tr>
    <tr>
      <td>ROC–AUC</td>
      <td>0.98</td>
    </tr>
  </tbody>
</table>

<p>Feature importance analysis showed that the most influential predictors of employee turnover were:</p>
<ul>
  <li>Satisfaction level.</li>
  <li>Number of projects.</li>
  <li>Years at company.</li>
  <li>Average monthly hours.</li>
  <li>Last evaluation score.</li>
</ul>

<h2>Key Insights</h2>
<ul>
  <li>Employees who left typically had <strong>lower satisfaction levels</strong>.</li>
  <li>Many employees who left were <strong>working long hours and managing multiple projects</strong>.</li>
  <li>A large proportion of departures occurred among employees with <strong>3–5 years of tenure</strong>.</li>
  <li>Higher salary levels were associated with <strong>lower turnover rates</strong>.</li>
  <li>Employees who received <strong>promotions rarely left the company</strong>.</li>
</ul>

<p>
These findings suggest that <strong>workload and job satisfaction are major drivers of employee attrition</strong>.
</p>

<h2>Recommendations</h2>
<ul>
  <li>Improve <strong>work–life balance</strong> by reducing excessive workloads and project assignments.</li>
  <li>Monitor employees with <strong>3–5 years of tenure</strong>, since turnover peaks during this period.</li>
  <li>Review company evaluation metrics that may implicitly reward <strong>long working hours</strong>.</li>
  <li>Increase opportunities for <strong>career advancement and promotions</strong>.</li>
  <li>Set clearer expectations about workload and company culture during employee onboarding.</li>
</ul>

<h2>Next Steps</h2>
<ul>
  <li>Cluster employees using <strong>K-means</strong> to identify groups with similar characteristics, specially for those with 3 years of employment.</li>
  <li>Evaluate models without the satisfaction variable if these surveys are not frequently done.</li>
  <li>Review evaluation metrics to make sure they are aligned with employees expectations.</li>
</ul>

<h2>Repository Contents</h2>
<pre><code>salifort-case-study/
├── salifort-motors-case-study-python.ipynb
├── figures
│   ├── confusion_matrix.png
│   ├── decision_tree_plot.png
│   └── feature_importance.png
└── README.md
</code></pre>

<h2>Technologies Used</h2>
<ul>
  <li>Python</li>
  <li>pandas</li>
  <li>NumPy</li>
  <li>seaborn</li>
  <li>matplotlib</li>
  <li>scikit-learn</li>
  <li>XGBoost</li>
</ul>

<h2>Project Type</h2>
<p>
Capstone project from the <strong>Google Advanced Data Analytics Professional Certificate</strong> demonstrating:
</p>
<ul>
  <li>Exploratory data analysis.</li>
  <li>Machine learning classification.</li>
  <li>Model evaluation.</li>
  <li>Business-oriented data insights.</li>
</ul>
