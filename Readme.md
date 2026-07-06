# Instructor Effectiveness Modeling (EdTech Context)

## Overview

This project analyzes instructor effectiveness using learner outcomes, engagement metrics, and feedback data from an EdTech platform.

The objective is to:

- Define an Instructor Effectiveness Score
- Aggregate batch-level data to instructor-level
- Create effectiveness tiers (Low, Medium, High)
- Train machine learning models to predict instructor effectiveness
- Interpret the factors influencing instructor performance

---

## Dataset

The dataset contains batch-level information for courses taught by different instructors.

### Identifier Columns

- batch_id
- instructor_id
- course_id

### Learner Outcome Metrics

- completion_rate
- dropout_rate
- avg_score_improvement
- avg_quiz_score

### Engagement Metrics

- avg_watch_time
- assignment_submission_rate
- forum_activity_rate

### Feedback Metrics

- avg_feedback_score
- feedback_response_rate

---

## Methodology

### 1. Exploratory Data Analysis (EDA)

Performed:

- Dataset overview
- Missing value analysis
- Distribution analysis
- Correlation heatmap

### 2. Instructor Effectiveness Definition

Instructor effectiveness was defined using a weighted scoring framework:

#### Learning Outcomes (50%)

- Completion Rate
- Dropout Rate
- Score Improvement

#### Engagement (30%)

- Watch Time
- Assignment Submission Rate
- Forum Activity Rate

#### Feedback (20%)

- Feedback Score
- Feedback Response Rate

The weighted score was used to create an overall Instructor Effectiveness Score.

### 3. Instructor-Level Aggregation

Batch-level data was aggregated using:

- Mean values for performance metrics
- Number of batches taught
- Number of unique courses taught

### 4. Tier Creation

Effectiveness scores were divided into:

- Low
- Medium
- High

using quantile-based binning.

### 5. Machine Learning Models

Models evaluated:

- Logistic Regression
- Random Forest Classifier

---

## Results

### Logistic Regression

Accuracy: 83.3%

### Random Forest

Accuracy: 91.7%

Random Forest achieved the best performance and was selected as the final model.

---

## Key Findings

Most influential features:

1. Dropout Rate
2. Completion Rate
3. Average Score Improvement
4. Feedback Response Rate
5. Average Feedback Score

The analysis indicates that learner retention and learning outcomes are the strongest indicators of instructor effectiveness.

---

## Limitations

- Course difficulty not available
- Instructor experience not available
- Learner demographics not available
- Effectiveness score based on assumed weights
- Historical performance trends not included

---

## Future Improvements

- Include course difficulty metrics
- Add instructor experience data
- Incorporate longitudinal performance trends
- Use advanced explainability methods such as SHAP

---

## Conclusion

This project successfully developed a framework for measuring instructor effectiveness using available learner, engagement, and feedback metrics.

The Random Forest model achieved 91.7% accuracy and identified learner retention and learning outcomes as the strongest predictors of instructor effectiveness.

The model should be used as a decision-support tool rather than a standalone instructor evaluation system.