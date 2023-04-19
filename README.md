# Job Posting Insights: Text Analytics & Firm Categorization

![MIT](https://badgen.net/badge/license/MIT/blue) ![Python3.9](https://badgen.net/badge/python/3.9/blue) ![Colab](https://badgen.net/badge/platform/Colab/orange?icon=chrome)

## Member

> Student: Shuyang Lin
> Instructor: Prof. Peter Haslag

## Background

This is a repo for the capstone project *Job Posting Insights: Text Analytics & Firm Categorization* in Spring 2023 at Vanderbilt University, Data Science Institute.

## Related Files

[Source Code](https://github.com/vandylins19/Spring_2023_DS_5999_Capstone_Shuyang_Lin_Job_Posting_Analytics/blob/main/Capstone_source_code.ipynb) Run on Google Colab

[Final Presentation Draft](https://docs.google.com/presentation/d/14QtMwKfsEuDOp8-7WoKooF17Hm4MAoXvUuG9pAdtLS0/edit?usp=sharing)


## Executive Summary
This capstone project aims to examine the applicability of text analytics to describe the pattern of companies in the job demand market. Distinguishing itself from prior research, this study uniquely combines elements of text analytics, company and industry perspectives on the job market, and a macro-level examination of employment trends.  A large dataset containing 607,795 rows of job descriptions from various companies and years was utilized. The analytics process includes the following steps: data cleaning, vectorizing, dimensionality reduction, clustering, visualization, topic modeling, and similarity score calculation. The output consists of two datasets: one with cluster labels for each company in a given year, representing the type of job demand, and another with pairwise cosine similarity scores for comparing job demands between companies in the same year or the same company across different years.

After cleaning the raw text by removing stopwords, numbers, and punctuation, the top 500 companies with the most job postings were selected for further analysis. The cleaned descriptions were concatenated by firm-year pairs and transformed into a vectorized format using TF-IDF with lemmatization.

TruncatedSVD was employed for dimensionality reduction to 100 dimensions. DBSCAN clustering proved ineffective, producing only one dense cluster and noise. K-means clustering resulted in 9 clusters identified using the elbow method. However, the silhouette scores indicated that some clusters were sparse.

T-SNE was used for visualization, revealing two well-distinguished clusters. Latent Dirichlet Allocation (LDA) was applied to extract topic words representing the clusters' themes. By linking industry names to the data, it was found that five clusters had a dominant industry (>50%). In contrast, the remaining clusters were composed of 2-3 industries. This result showed that it’s possible to apply text analytics to classify the “job demand group” of companies.

Finally, cosine similarity scores were calculated for pairwise comparisons between companies in the same year and the same company across different years. The results were saved in a CSV file for future analysis.
