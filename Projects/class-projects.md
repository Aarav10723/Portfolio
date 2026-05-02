# Projects for Class

## Project 1 — Exploratory Data Analysis: Netflix Catalog

**Research Question**  
How has Netflix’s content library evolved over time in terms of content type, genres, and geographic distribution?

**Overview**  
This project analyzes how Netflix’s catalog has changed over time using exploratory data analysis. The study examines trends in content growth, differences between movies and TV shows, genre distribution, and geographic representation to understand how a global streaming platform evolves.

**Dataset**  
Netflix Movies and TV Shows dataset (Kaggle — Shivam Bansal)

**Tools Used**  
Python, pandas, matplotlib, Jupyter Notebook

### Deliverables
[View Code & Report](https://aarav10723.github.io/ds2-project1-netflix/)


## Project 2 — Predicting Student Success Using Machine Learning

**Dataset**
Kaggle Dataset - Student Performance Prediction, by Amr Maree. (https://www.kaggle.com/datasets/amrmaree/student-performance-prediction)

**Introduction: Why this Matters**
Every semester, some students struggle and fall behind, but often it’s not obvious who needs help until it’s too late. What if we could predict student performance early using data? In this project, I explored whether machine learning models can predict whether a student will pass or fail a course based on factors like study time, attendance, and past performance. The goal is to understand which factors matter most and how accurately we can identify at-risk students. This matters because early predictions could help schools provide support before students fall behind.

**Research Question**
Can we predict whether a student will pass or fail using behavioral and academic data? More importantly which factors have the biggest impact on student success?

**Key Findings**
1. Students don’t start from scratch, their academic history strongly predicts their future performance. Those who entered the course with higher prior grades consistently continued to succeed, while those with weaker academic foundations struggled to catch up. This suggests that performance is not just about current effort, but also about momentum built over time. Below I have attached a picture representing the predicted scores based on previous exams and the acutal scores.
<img width="690" height="490" alt="image" src="https://github.com/user-attachments/assets/d68b673d-9b6a-434b-b1ec-7230dfd425b7" />

2. At first, increasing study time leads to noticeable improvements in performance. However, after a certain point, the benefits begin to level off, indicating that simply studying more does not guarantee better results. This highlights the importance of efficient studying rather than just longer hours. Here I have also attached a graph showing us the correlation between study hours and the final exam scores.
<img width="610" height="468" alt="image" src="https://github.com/user-attachments/assets/151f7ec1-caf1-437b-8c72-70a608164f60" />

3. Attendance emerged as one of the most critical factors. Students with frequent absences were significantly more likely to fail, suggesting that missing class creates a gap that is difficult to recover from, regardless of other factors like study time. In the graph below you can see how missing attendance assumes to predict failure.
<img width="540" height="391" alt="image" src="https://github.com/user-attachments/assets/040af092-dd33-49a7-9ef1-e513edf85100" />


**What I learned**
This project showed me that machine learning is not just about accuracy. It’s about understanding why predictions happen. Even simple models can reveal important patterns, but comparing multiple models gives a much clearer picture.

**Why the results Matter**
The most important insight is that early indicators already exist. Schools don’t need new data, they just need better ways to use it. With models like this, educators could: Identify struggling students early, Provide targeted support & Improve overall success rates. Machine learning can effectively predict student outcomes and highlight key factors like past performance and attendance. While no model is perfect, these tools can help shift education from reactive to proactive.

**Code:**
[project2_student_performance_ml.html](https://github.com/user-attachments/files/26455455/project2_student_performance_ml.html)

**Technical Report**
[Project 2 Technical Report.pdf](https://github.com/user-attachments/files/26486301/Project.2.Technical.Report.pdf)


## Final Project - Finding Patterns in the Chaos: Building an AI Stock Recommendation System

**Introduction:**
For the everyday investor, the stock market can feel like a chaotic ocean of numbers, flashing screens, and unpredictable swings. One of the biggest challenges investors face is identifying which stocks actually behave similarly to one another. Many people want to build portfolios where their investments move in a coordinated, predictable direction, but finding those hidden connections manually across thousands of companies is nearly impossible.
For our project, we set out to answer a specific question: Can we use an unsupervised machine learning model to automatically group stocks that behave alike, and use those groups to create a recommendation system? 
Our goal was to take the guesswork out of finding related stocks, giving investors a clearer, data driven lens through which to view the market.

**The Data & Feature Engineering:**
To understand how stocks move, we built an automated pipeline to gather 10 years of daily price data for 243 different NASDAQ companies. However, simply looking at a stock's daily closing price isn't enough to understand its true "personality." We engineered specific indicators to capture a fuller picture of how these companies operate:
 - Long-Term Reliability & Risk: We measured historical average performance, volatility, worst-case historical drops (Max Drawdown), and risk-adjusted returns (Sharpe Ratio).
 - Short-Term Momentum: We tracked recent 30-day and 90-day streaks to see how the stock was behaving right now.
 - Market Alignment: We measured how closely each stock mirrored the broader market (the S&P 500).
Because these metrics exist on wildly different scales, we standardized the data so that every feature carried an equal weight when fed into the model.

**Cutting through the Noise:**
Because we gave the AI so much complex information, we first used a statistical technique called Principal Component Analysis (PCA) to simplify the dataset. This mathematically strips away the random "noise" of the market while keeping the core behavioral signals intact.
When we analyzed what the model was prioritizing, the results were fascinating. The model revealed that a stock's long-term historical risk and return profile represents the primary difference among equities (accounting for 60% of the variance), while its recent short-term price momentum operates as a distinct, secondary factor (20% variance).

<img width="244" height="323" alt="image" src="https://github.com/user-attachments/assets/d47308ba-c5df-45e7-86e5-4d3b2edddb74" />





