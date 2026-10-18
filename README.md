# Redlining and Walkability in Portland, Oregon

Do neighborhoods that were redlined in the 1930s have lower
walkability today? This project tests that question across 68 Portland
neighborhoods using regression analysis in R.

[Read the full report (PDF)](report/Legacy%20in%20the%20Lines.pdf)

## Key findings
- Contrary to my hypothesis, formerly redlined neighborhoods (Grades
  B–D) scored roughly 20–46 points higher on walkability than
  Grade A neighborhoods, across all models.
- Greater walkability in formerly redlined neighborhoods doesn’t mean the people harmed by redlining are the ones benefiting. Planning decisions and gentrification may have displaced many residents of color from these neighborhoods.
- Within neighborhoods of the same HOLC grade, higher concentrations of people of color were associated with lower walkability, suggesting walkability is not equally distributed.

## Methods
I compared walkability scores (City of Portland Complete Neighborhoods
index) across 68 neighborhoods with HOLC grades A-D using OLS regression.
Models test both a binary redlined indicator and categorical grades
(Grade A as reference), with vulnerability, percent people of color, and
income as controls. After VIF checks showed multicollinearity among the
controls, I re-ran models with them entered separately. Diagnostics
included Breusch-Pagan and Shapiro-Wilk tests, heteroskedasticity-robust
(HC3) standard errors, and a sensitivity check excluding Forest Park.

<img width="907" height="701" alt="image" src="https://github.com/user-attachments/assets/ff009916-503e-4a76-8819-c51bce2b3985" />


## Data
- HOLC redlining grades: https://dsl.richmond.edu/panorama/redlining/data
- Walkability: City of Portland Complete Neighborhoods index
