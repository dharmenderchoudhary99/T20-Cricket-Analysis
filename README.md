# End-to-End Sports Data Analytics Project

    ## Project Overview

    This project demonstrates a comprehensive end-to-end sports data analytics workflow using data from the T20 World Cup cricket matches. The project encompasses web scraping from the
    ESPN Cricinfo website, data cleaning and transformation using Python and Pandas, and data analysis and visualization using Power BI. 

    ## Tools and Technologies

    - **Python**: For data extraction, cleaning, and transformation
    - **Pandas**: For data manipulation and analysis
    - **Power BI**: For data modeling, analysis, and visualization

    ## Project Structure

    1. **Web Scraping and Data Extraction**
    2. **Data Cleaning and Transformation in Python**
    3. **Data Modeling and Analysis in Power BI**

    ## Data Cleaning and Transformation in Python

    ### Importing the Dataset

    ```python
    import pandas as pd
    import json

    # Importing the match results dataset
    with open('t20_json_files/t20_wc_match_results.json') as f:
        data = json.load(f)
    df_match = pd.DataFrame(data[0]['matchSummary'])
    df_match.head()
    df_match.shape
    df_match.rename({'scorecard':'match_id'}, axis=1, inplace=True)

    Data Transformation in Power Query
    In Power BI, the following data transformation steps were performed using Power Query:

    Promoted Header: Promoted the first row to header.
    Extracted Text Before Delimiter: Extracted relevant text before specific delimiters.
    Trimmed Text: Trimmed unnecessary spaces from text fields.
    Removed Duplicates: Removed duplicate records to ensure data integrity.
    Data Modeling and Building Parameters Using DAX
    In Power BI, the following steps were taken:

    Data Modeling: Created relationships between different tables to build a coherent data model.
    DAX Calculations: Used Data Analysis Expressions (DAX) to build calculated columns and measures to enhance data analysis capabilities.
    Conclusion
    This project showcases the process of extracting, cleaning, transforming, and analyzing sports data from the T20 World Cup cricket matches. By leveraging Python for data manipulation and Power BI for data visualization, we can derive meaningful insights from raw data, ultimately enhancing data-driven decision-making.

    Future Work
    Integrate additional data sources for a more comprehensive analysis.
    Implement advanced machine learning models to predict match outcomes and player performance.
    Enhance visualizations with interactive dashboards and reports.
    Author
    Dharmender Choudhary
