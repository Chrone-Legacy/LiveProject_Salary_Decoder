#Bangalore Tech Salary Decoder

##  Overview
An end-to-end data engineering and HR analytics pipeline that cleans, standardizes, and analyzes a messy dataset of 1,000 Bengaluru tech professionals. Built as part of a rapid 2-hour live industry sprint, this project transforms highly fragmented, unstructured payroll records into a clean, terminal-based market intelligence report.

The primary objective was to extract actionable salary insights regarding role ceilings, experience growth velocity, company-type premiums, and individual pay anomalies using strictly fundamental data manipulation techniques.

##  Tech Stack & Constraints
This project was executed under strict technical constraints to demonstrate mastery of core data manipulation without relying on external shortcuts:
* **Language:** Python 3
* **Libraries:** Pandas, NumPy
* **Strict Limitations:** *  No Regular Expressions (`import re`) allowed for string parsing.
  *  No Machine Learning (ML) or predictive modeling.
  *  No external charting/visualization libraries (e.g., Plotly, Matplotlib). All outputs are formatted as clean ASCII console reports.

##  Key Engineering Features
* **Custom Numeric Parsers:** Engineered a custom, non-regex algorithm to safely parse and scale erratic salary strings (e.g., `'15,50,000'` and `'15.5 LPA'`) into unified float metrics, while preserving critical `NaN` values for entry-level professionals.
* **Categorical Standardization:** Built hardcoded mapping dictionaries to consolidate fragmented role titles (e.g., standardizing `'BE'`, `'Backend Dev'`, and `'Backend Engineer'` to a canonical `'SDE Backend'` label) to prevent analytical fragmentation.
* **Statistical Anomaly Detection:** Leveraged optimized Pandas vector operations (`.groupby()` combined with `.transform()`) to cross-reference multi-dimensional cohorts (Role + Company Type + Experience) to isolate statistically underpaid professionals relative to their exact local peers.
* **Dynamic ASCII Dashboarding:** Utilized advanced Python f-string formatting with explicit width specifiers to construct a perfectly aligned, dynamically generated terminal reporting UI.

##  Key Market Insights Extracted
1. **The Scale-Up Ceiling:** Unicorn startups establish the industry pay ceiling, commanding a **26.4 LPA** median for backend engineers, while traditional MNCs subject identical roles to a **23% pay discount**.
2. **Early-Career Velocity:** The transition from entry-level (0-1 years) to early-career (1-3 years) triggers the largest compensation surge in the engineering lifecycle, resulting in a **+68% wage growth**.
3. **Internal Pay Inequities:** Granular cohort analysis surfaced severe enterprise loyalty discounts, identifying mid-level engineers operating at deficits of up to **-5.2 LPA** below their direct local peer medians.

##  How to Run Locally
1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/YourUsername/Bangalore-Tech-Salary-Decoder.git](https://github.com/YourUsername/Bangalore-Tech-Salary-Decoder.git)
