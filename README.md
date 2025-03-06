# EDA-with-Mysql
##Layoffs Data Exploratory Analysis

Project Overview

This project performs exploratory data analysis (EDA) on the layoffs_staging2 dataset. The dataset contains information about company layoffs, including total layoffs, percentage of workforce laid off, industry, country, and financial details.

SQL Queries Breakdown

1. Initial Data Exploration

Retrieves all records for an initial understanding of the dataset.

2. Key Statistics

Identifies the highest number of layoffs and the maximum percentage of employees laid off using MAX() function.

3. Companies with 100% Layoffs

Lists companies that laid off their entire workforce, sorted by the highest layoffs.

Lists companies that laid off their entire workforce, sorted by total funds raised.

4. Total Layoffs by Company

Summarizes total layoffs per company using SUM(total_laid_off), sorted in descending order.

5. Date Range

Determines the earliest and latest dates in the dataset using MIN(date) and MAX(date).

6. Industry and Country Trends

Summarizes total layoffs per industry and country using SUM(total_laid_off), grouped by industry and country respectively.

7. Yearly Layoff Trends

Calculates layoffs per year using YEAR(date) function and SUM(total_laid_off), grouped by year.

8. Layoffs by Startup Stage

Analyzes layoffs based on startup growth stages using GROUP BY stage and SUM(total_laid_off).

9. Monthly Layoff Trends

Aggregates layoffs by month using SUBSTRING(date,1,7) to extract year-month and SUM(total_laid_off), grouped accordingly.

10. Rolling Total of Layoffs

Computes cumulative layoffs over time using a Common Table Expression (CTE) and SUM() OVER(ORDER BY month) for running totals.

11. Top 5 Companies with Most Layoffs Each Year

Uses Common Table Expressions (CTEs) and ranking functions like DENSE_RANK() OVER(PARTITION BY year ORDER BY layoffs DESC) to identify the top companies with the most layoffs per year.

Conclusion

This exploratory data analysis provides insights into:

The industries and companies most affected by layoffs.

Layoff trends over time (monthly, yearly, and cumulative totals).

The impact of funding on layoffs.

The correlation between startup stage and layoffs.

These insights help stakeholders understand economic downturns, employment trends, and industry-wide impacts.

Requirements

SQL database (e.g., MySQL, PostgreSQL, SQL Server)

layoffs_staging2 table with relevant fields (date, company, total_laid_off, percentage_laid_off, industry, country, funds_raised_millions, stage).

Future Work

Further analysis on layoffs based on company size.

Correlation between layoffs and economic events (e.g., recessions, market crashes).

Data visualization using Power BI, Tableau, or Python libraries (Matplotlib, Seaborn).

Author: Collins Kipchirchir RonoDate: March 2025

