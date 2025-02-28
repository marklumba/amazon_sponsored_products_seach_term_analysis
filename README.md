# Advertising Performance Analysis

## Overview

This project analyzes advertising performance data by categorizing targeting types, calculating key metrics, and visualizing trends. It provides comprehensive insights into overall performance, campaign and ad group effectiveness, targeting types, and keyword analysis.

---

## Features

1. **Targeting Categorization**
   - Categorizes values in the `Targeting` column:
     - If the value starts with `asin=`, it is categorized as `ASIN`.
     - If the value starts with `category=`, it is categorized as `Category`.
     - If the value is exactly `*`, it is categorized as `Auto`.
     - Otherwise, it is categorized as `Other`.
   - Applies the categorization to a new column named `Targeting Type`.

2. **Analysis 1: Overall Performance**
   - Calculates key metrics:
     - Total Spend
     - Total Sales (7 Day Total Sales)
     - Total Impressions
     - Total Clicks
     - Average CTR (Click-Through Rate)
     - Average CPC (Cost Per Click)
     - Average ACOS (Advertising Cost of Sale)
     - Average ROAS (Return on Advertising Spend)
   - Outputs results as a formatted DataFrame (`df_overall_performance`).

3. **Analysis 2: Performance by Campaign**
   - Groups data by `Campaign Name`.
   - Calculates sum totals for Spend, Sales, Impressions, and Clicks.
   - Computes the ROAS for each campaign.
   - Sorts campaigns by Spend in descending order.
   - Outputs the top 5 campaigns in a DataFrame (`df_performance_by_campaign`).

4. **Analysis 3: Performance by Ad Group**
   - Groups data by `Ad Group Name`.
   - Calculates sum totals for Spend, Advertised SKU Sales, and Other SKU Sales.
   - Computes Total Sales and ROAS for each ad group.
   - Sorts ad groups by Spend in descending order.
   - Outputs the top 5 ad groups in a DataFrame (`df_performance_by_adgroup`).

5. **Analysis 4: Performance by Targeting Type**
   - Groups data by `Targeting Type`.
   - Calculates sum totals for Spend, Sales, Impressions, and Clicks.
   - Computes ROAS for each targeting type.
   - Outputs the results in a DataFrame (`df_performance_by_targetingtype`).

6. **Analysis 5: Top Keywords for Auto Campaigns**
   - Filters for auto campaigns (`Targeting == '*'`).
   - Groups data by `Customer Search Term`.
   - Calculates sum totals for Spend, Sales, Impressions, and Clicks.
   - Computes ROAS for each keyword.
   - Sorts keywords by Spend in descending order.
   - Outputs the top 5 keywords in a DataFrame (`df_performance_by_autocampaigns`).

7. **Analysis 6: Cross-Selling Analysis**
   - Calculates cross-selling metrics:
     - Total Advertised SKU Sales
     - Total Other SKU Sales
     - Cross-Sell Ratio (Other SKU Sales / Advertised SKU Sales)
   - Outputs results in a formatted DataFrame (`df_cross_selling_analysis`).

8. **Visualization: Daily Spend and Sales Trend**
   - Groups data by `Date` and calculates daily Spend and Sales.
   - Generates a line plot:
     - Blue line: Spend
     - Green line: Sales
   - Includes axis labels, title, and legend for clarity.

---

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/advertising-performance-analysis.git
    cd advertising-performance-analysis
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

1. Prepare your input data as a CSV file with columns including:
   - `Date`, `Campaign Name`, `Ad Group Name`, `Targeting`, `Spend`, `7 Day Total Sales`, `Impressions`, `Clicks`, `7 Day Advertised SKU Sales`, `7 Day Other SKU Sales`, `Customer Search Term`

2. Run the analysis script:

    ```bash
    python analyze_ad_performance.py
    ```

3. View the output DataFrames and visualization.

---

## Output

- Summary DataFrames for overall performance, campaign and ad group analysis.
- Top keywords for auto campaigns.
- Cross-selling analysis metrics.
- Line plot showing daily spend and sales trends.

---

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
