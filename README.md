# Global-AI-Workforce-Intelligence-Dashboard

## Project Overview

Artificial Intelligence is reshaping economies faster than any previous technological shift. While AI creates new opportunities for productivity and innovation, it also introduces significant workforce disruption, changing skill requirements, employment patterns, and investment priorities across industries and countries.

This project analyzes a global AI workforce dataset to understand how AI adoption is influencing labor markets, economic performance, workforce vulnerability, and organizational readiness.

The goal was not simply to visualize the data, but to build an executive decision-support dashboard capable of answering strategic questions such as:

- Which countries are leading AI adoption?
- Which industries face the highest automation risk?
- Are governments investing enough in workforce reskilling?
- Does higher AI adoption actually improve productivity?
- Which countries require immediate intervention?
- What actions should policymakers and business leaders prioritize?

The final solution consists of five interactive Power BI dashboards that progressively guide decision makers from global trends to detailed workforce risks, economic impacts, and actionable recommendations.

Rather than presenting isolated charts, the dashboards were designed as a storytelling experience, allowing users to move from high-level indicators into deeper analysis before concluding with executive insights and strategic recommendations.

## Data Understanding & Exploration (EDA)

Before designing any dashboards, an exploratory data analysis (EDA) was performed to understand the structure, quality, and reliability of the dataset. This step ensured that the visualizations would answer meaningful business questions rather than simply display available data.

Dataset Overview

The dataset contains AI adoption and workforce indicators collected across multiple countries, industries, skill categories, and quarterly time periods.

It includes metrics related to:

AI adoption rate
Productivity score
AI efficiency index
Workforce displacement risk
Jobs created and jobs displaced
Reskilling investment
AI policy maturity
Digital infrastructure
Automation susceptibility
Wage change
Workforce size
Leadership and readiness indicators

The data follows a star-schema design consisting of one fact table and multiple supporting dimension tables.

Data Quality Assessment

The dataset was examined for common data quality issues before any analysis was performed.

The assessment included:

Checking for missing values
Identifying duplicate records
Reviewing inconsistent data types
Detecting invalid or extreme values
Validating relationships between tables
Confirming referential integrity of dimension tables

Only a very small percentage of records contained missing values, primarily within wage-related metrics. These were left as blanks rather than artificially imputed to avoid introducing analytical bias.

No duplicate observations affecting analysis were identified.

Exploratory Analysis

Initial exploration focused on understanding the overall behavior of the data before creating KPIs or dashboards.

Key questions investigated included:

Which countries have the highest AI adoption?
Which industries experience the greatest automation risk?
How does productivity relate to AI adoption?
Are developed economies adopting AI differently from emerging economies?
Which skill categories are most exposed to workforce disruption?
Does higher reskilling investment correlate with improved employment outcomes?

Summary statistics were calculated for major numerical variables including:

Mean
Median
Minimum
Maximum
Standard deviation

Distribution plots and summary tables helped identify variables with wide variation across countries and industries.

Correlation Analysis

Relationships between numerical variables were explored to identify meaningful patterns.

Particular attention was given to correlations between:

AI Adoption ↔ Productivity
AI Adoption ↔ AI Efficiency
Automation Susceptibility ↔ Workforce Displacement
Reskilling Investment ↔ Jobs Created
AI Policy Maturity ↔ Productivity
Digital Infrastructure ↔ AI Readiness

The analysis revealed that AI adoption alone is not sufficient to achieve better workforce outcomes. Countries combining strong AI policy, digital infrastructure, and sustained reskilling investment consistently demonstrated stronger productivity and efficiency.

Key Findings from EDA

The exploratory analysis uncovered several important trends that later shaped the dashboard design:

AI adoption varies significantly across countries and industries.
Technical and digital occupations exhibit the highest AI adoption rates.
Manual and administrative occupations experience the highest displacement risk.
Countries with stronger AI governance generally achieve higher productivity scores.
Industries with high automation susceptibility do not always invest proportionally in workforce reskilling.
Workforce outcomes depend on multiple factors rather than AI adoption alone.

These findings guided the selection of KPIs, calculated measures, and dashboard layouts, ensuring that every visualization answered a specific analytical question instead of simply presenting descriptive statistics.

## Data Preparation & Transformation

Before any analysis was performed, the raw dataset was prepared using Power Query to ensure consistency, reliability, and efficient reporting. The objective was to create a clean analytical model that supports accurate calculations and interactive dashboard performance.

Data Import

The dataset was imported into Power BI and organized into a star schema consisting of:

Fact Table
fact_workforce_ai_index
Dimension Tables
dim_country
dim_industry
dim_skill_category
dim_date

This structure improves query performance, simplifies DAX calculations, and follows Power BI data modeling best practices.

Data Cleaning

Several preprocessing steps were completed before modeling the data.

Data Type Validation

All columns were reviewed and converted to appropriate data types.

Examples include:

Whole Numbers
Decimal Numbers
Percentages
Currency
Dates
Boolean values
Text fields

Correct data types ensure accurate aggregations and calculations throughout the report.

Missing Values

The dataset contained a small number of missing observations within:

Average Wage Change (%)
AI Tool Usage Hours per Week

Since these represented unavailable survey responses rather than incorrect data, they were preserved as blank values instead of being imputed. This prevents introducing artificial bias into the analysis.

Data Validation

The dataset was inspected for:

Duplicate records
Null primary keys
Invalid relationships
Outliers
Inconsistent categorical values

No significant integrity issues affecting the analysis were identified.

Data Modeling

The report was designed using a star schema, with the fact table connected to four dimension tables through one-to-many relationships.

The model enables filtering and drill-down analysis across:

Country
Industry
Skill Category
Time

This approach minimizes redundancy while maximizing reporting flexibility.

Calendar Table

A dedicated Calendar Table was created to support robust time intelligence calculations.

The calendar includes:

Date
Year
Quarter
Month
Quarter Labels
Year-Quarter hierarchy

This table was marked as the official Date Table in Power BI and used throughout the report for trend analysis and year-over-year comparisons.

Feature Engineering

To support executive reporting, several additional business metrics were derived from the raw data.

Examples include:

Net Jobs Created
AI Efficiency Index
Productivity Score
Workforce Displacement Risk
Reskilling Investment per Job
Priority Scores
Leadership Status
Investment Priority
Reskilling Priority

These calculated metrics transformed operational data into business-oriented KPIs suitable for executive decision-making.

Data Quality Outcome

After preparation, the dataset was:

Clean and standardized
Fully relational
Optimized for analytical reporting
Ready for DAX calculations
Structured to support interactive filtering and drill-down analysis

This preparation phase established a reliable analytical foundation for the five Power BI dashboards developed throughout the project.

## Dashboard Development

The reporting solution consists of five interactive dashboards, each designed to answer a different strategic business question. Rather than displaying isolated visualizations, the dashboards follow a storytelling approach that guides users from understanding global AI adoption trends to identifying workforce risks, evaluating readiness, measuring economic outcomes, and finally generating actionable recommendations.

Dashboard 1 – Global AI Adoption & Workforce Impact
<img width="2075" height="1200" alt="AI Adoption_page-0001" src="https://github.com/user-attachments/assets/f173e3d1-3239-4575-bcfb-37478a54ca28" />

Objective

The first dashboard provides a high-level overview of global AI adoption and workforce transformation. It establishes the analytical foundation for the report by summarizing adoption trends, productivity, workforce displacement, and reskilling investment across countries, industries, and skill categories.

This dashboard answers the following questions:

How widely has AI been adopted globally?
Has AI adoption accelerated over time?
Which countries are leading AI adoption?
Which industries demonstrate the highest productivity gains?
Which skill categories benefit the most from AI adoption?
Key Performance Indicators (KPIs)

The dashboard begins with executive KPI cards summarizing the current state of AI adoption.

The KPIs include:

Average AI Adoption Rate (%)
Average Productivity Score
Average Displacement Risk
Net Jobs Created
Total Reskilling Investment

Each KPI includes year-over-year comparison indicators to highlight changes relative to the previous year.

Visualizations
Global AI Adoption Map

A filled map displays the average AI adoption rate by country, enabling users to quickly identify geographic adoption patterns and regional disparities.

AI Adoption Trend

A line chart illustrates quarterly AI adoption trends between 2021 and 2024. An annotation highlights the emergence of mainstream Generative AI in late 2022, allowing users to observe changes following its widespread adoption.

Productivity by Industry

A ranked bar chart compares productivity impact scores across industries, highlighting sectors experiencing the greatest productivity improvements from AI implementation.

AI Adoption by Skill Category

A horizontal bar chart compares AI adoption rates across workforce skill categories, illustrating which occupations are integrating AI most successfully.

Business Insights

Several key observations emerged from this dashboard:

AI adoption has increased steadily throughout the reporting period, with accelerated growth following the emergence of Generative AI.
Adoption levels differ considerably across countries, indicating uneven digital transformation.
Productivity improvements are concentrated within industries actively investing in AI technologies.
Technical and digital skill categories exhibit the highest AI adoption, suggesting greater compatibility with AI-assisted workflows.
Increased AI adoption is accompanied by higher reskilling investment, indicating growing recognition of workforce transformation challenges.
Business Value

This dashboard provides executives with a comprehensive overview of the current AI landscape. It serves as the starting point for the report by identifying global adoption patterns before investigating workforce risks, organizational readiness, economic impacts, and strategic recommendations in subsequent dashboards.

Dashboard 2 — Workforce Risk & Vulnerability
<img width="2075" height="1200" alt="AI Adoption_page-0002" src="https://github.com/user-attachments/assets/9757eb44-e708-45db-ac51-affc3b125db8" />


Business Question

Which countries, industries and workforce segments are most vulnerable to AI disruption?

This dashboard shifts the analysis from adoption toward risk exposure.

Its purpose is to identify where AI creates the greatest workforce displacement and which areas require immediate intervention.

Executive KPIs

The dashboard summarizes workforce vulnerability using:

Average Displacement Risk
Workers at High Risk
Highest Risk Industry
High Risk Countries
Net Jobs Lost

Each KPI includes year-over-year performance and trend indicators.

Visualizations
Industry Risk Heatmap

A country-by-industry heatmap highlights displacement risk across economic sectors.

The heatmap enables quick identification of industries consistently exposed to automation across multiple countries.

Countries with Highest Workforce Loss

Ranks countries according to estimated workforce displacement.

This immediately identifies the regions experiencing the largest employment losses.

Displacement Risk by Skill Category

Ranks workforce skill categories by average displacement risk.

The analysis shows that:

Manual & Physical occupations experience the greatest automation risk.
Administrative roles remain highly vulnerable.
Creative and analytical occupations demonstrate comparatively lower displacement risk.
Workforce Distribution by Risk Level

A donut chart segments the workforce into:

Low Risk
Moderate Risk
High Risk
Very High Risk

This provides a simple overview of global workforce exposure.

AI Adoption vs Workforce Displacement Risk

A scatter plot compares AI adoption with displacement risk while separating developed and emerging economies.

The visualization shows that:

Higher AI adoption does not necessarily imply higher displacement.
Policy maturity and workforce readiness appear to moderate employment risk.
Several emerging economies combine relatively high displacement with only moderate adoption, indicating lower preparedness.
Key Insights
Workforce risk remains concentrated in highly automatable industries.
Manual occupations face the greatest disruption.
Countries differ significantly in their ability to absorb AI-driven workforce changes.
AI adoption alone is not the primary driver of displacement—investment in reskilling and policy maturity also play a critical role.

Dashboard 3 — AI Adaptation & Readiness
<img width="2075" height="1200" alt="AI Adoption_page-0003" src="https://github.com/user-attachments/assets/a82f2058-adb1-4c23-93a6-6eaf2e77112c" />


Business Question

Which countries and industries are adapting most effectively to AI transformation?

While Dashboard 2 focuses on risk, this dashboard evaluates preparedness. It measures how effectively countries convert AI adoption into productivity gains through investment, policy, and workforce development.

Executive KPIs

The dashboard highlights five indicators of AI readiness:

AI Efficiency Index
Productivity Score
Top AI Leader (Country)
Top Performing Industry
AI Tool Usage

These KPIs provide an at-a-glance view of the strongest performers in AI transformation.

Visualizations
AI Adoption vs Productivity

A bubble scatter plot compares AI adoption with productivity scores across countries while distinguishing developed and emerging economies.

This visualization helps identify countries achieving strong productivity gains relative to their AI adoption levels.

Jobs Displaced vs Jobs Created by Skill Category

A diverging bar chart compares jobs lost against jobs created across workforce skill groups.

It illustrates that although AI displaces jobs in many categories, technical and knowledge-based occupations generate substantially more new opportunities than manual roles.

AI Tool Usage Over Time

A multi-line chart compares AI tool usage trends between developed and emerging markets.

The chart highlights increasing adoption across both groups while showing developed economies generally maintaining higher usage levels.

Reskilling Investment by Country

A ranked bar chart identifies countries making the largest investments in workforce reskilling.

Higher investment levels are associated with stronger AI readiness and improved workforce adaptability.

Productivity Score by AI Policy Maturity

A column chart compares average productivity scores across AI policy maturity levels.

Countries with more established AI governance consistently achieve higher productivity outcomes, reinforcing the importance of policy alongside technology adoption.

Key Insights
AI readiness depends on more than adoption alone; governance and workforce investment are equally important.
Countries investing heavily in reskilling generally achieve stronger AI efficiency.
Technical and analytical occupations generate more AI-enabled employment opportunities than manual occupations.
Mature AI policy frameworks are associated with higher productivity performance.

Dashboard 4 — Economic Impact & Workforce Outcomes
<img width="2075" height="1200" alt="AI Adoption_page-0004" src="https://github.com/user-attachments/assets/44ac58b4-033e-493f-b99a-1102a438285a" />


Business Question

How is AI reshaping employment, wages, investment, and economic performance?

This dashboard examines the broader economic consequences of AI adoption by connecting workforce outcomes with investment behavior and industry performance.

Executive KPIs

The dashboard summarizes macroeconomic impact using:

Average Wage Change
Jobs Created Ratio
Net Employment Change
Investment per Net Job
Workforce Exposed to AI

These metrics provide a high-level assessment of AI’s economic influence.

Visualizations
Automation Susceptibility vs AI Investment

A quadrant-based bubble chart compares automation susceptibility with AI investment levels.

The chart classifies industries into strategic groups such as:

Strategic Leaders
Future Ready
Underprepared High Risk
Low Priority

This enables rapid identification of sectors requiring policy or investment attention.

Wage Change by Industry

A horizontal bar chart compares average wage growth across industries.

Professional Services and Healthcare demonstrate stronger wage improvements, while Consumer industries exhibit more modest gains.

Jobs Created vs Jobs Displaced

A donut chart summarizes the overall balance between employment creation and displacement.

It emphasizes that workforce losses currently exceed newly created roles, underscoring the need for continued workforce transition initiatives.

Reskilling Investment vs Jobs Created

A scatter plot evaluates whether higher workforce investment translates into greater job creation.

The relationship suggests a positive trend, although significant variation exists between countries and development tiers.

Key Insights
AI investment alone does not guarantee favorable workforce outcomes.
Industries combining high automation risk with limited investment remain the most vulnerable.
Wage growth varies considerably across sectors.
Reskilling investment appears positively associated with employment creation, reinforcing the value of workforce development strategies.

Dashboard 5 — Insights & Strategic Recommendations
<img width="2075" height="1200" alt="AI Adoption_page-0005" src="https://github.com/user-attachments/assets/390aaf76-8e8b-4cd9-a4b8-c1e076050bde" />


Business Question

Based on the complete analysis, what actions should decision-makers prioritize?

The final dashboard consolidates analytical findings into actionable business recommendations, transforming descriptive analytics into decision support.

Executive KPIs

The dashboard summarizes strategic priorities through:

High Risk Countries
Industries Requiring Investment
Critical Skill Categories
Countries Showing Improvement
AI Leaders

These indicators provide an immediate overview of global priorities.

Decision Support Tables

The dashboard includes four analytical tables designed for operational decision-making:

Countries Needing Immediate Attention — ranks countries using AI adoption, displacement risk, reskilling investment, and an overall priority score.
Industries Needing Investment — identifies sectors where automation risk outpaces AI investment and provides recommended actions.
Skills Requiring Reskilling — highlights workforce groups with high replaceability, estimated training duration, augmentation potential, and recommended interventions.
Executive Summary — consolidates the project's key findings and strategic recommendations into a concise decision brief for stakeholders.
Key Strategic Findings
AI adoption continues to improve globally, but workforce risk remains concentrated in highly automatable industries.
Technical & Digital skills exhibit the highest adoption rates, while Manual & Physical work experiences the greatest displacement risk.
Countries with stronger AI policy maturity and sustained reskilling investment consistently achieve higher productivity and AI efficiency.
Several industries remain highly susceptible to automation despite below-average AI investment, highlighting future disruption risks.
Strategic Recommendations
Increase reskilling investment in high-risk industries.
Prioritize workforce transition for manual and administrative occupations.
Strengthen AI governance alongside technology adoption.
Expand digital infrastructure and STEM talent development to improve long-term workforce resilience.

# Business Recommendations

Based on the analysis, organizations should:

• Increase investment in workforce reskilling before large-scale AI deployment.

• Prioritize AI adoption in industries with high productivity potential but relatively low displacement risk.

• Develop AI governance frameworks alongside technology implementation.

• Expand digital infrastructure and STEM education to improve long-term workforce readiness.

• Continuously monitor AI adoption and workforce impact through KPI dashboards rather than one-time assessments.

# Skills Demonstrated

Business Intelligence

• Dashboard Design
• KPI Development
• Data Storytelling
• Executive Reporting

Data Analytics

• Data Cleaning
• Data Transformation
• Exploratory Data Analysis (EDA)
• Statistical Analysis
• Trend Analysis

Power BI

• Data Modeling
• Star Schema
• DAX Measures
• Interactive Filtering
• Drill-through
• Custom Tooltips
• KPI Cards
• Conditional Formatting
• Bookmarks
• Maps
• Scatter Charts
• Heatmaps

Business Analysis

• Requirement Gathering
• Insight Generation
• Strategic Recommendations
• Decision Support Reporting

# Tools

• Power BI Desktop
• Power Query
• DAX
• Microsoft Excel

## Author

Abdelrahman Ayman

Business Informatics Student

Aspiring Revenue Operations & Data Analytics Professional

LinkedIn: linkedin.com/in/abdelrahman-ayman-b41a76265/
