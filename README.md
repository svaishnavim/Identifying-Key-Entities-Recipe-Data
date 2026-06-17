# Identifying-Key-Entities-Recipe-Data

Problem Statement:  Develop a custom Named Entity Recognition (NER) model to identify and extract key elements from recipe text (such as ingredients, quantities and units of measurement).

Tasks:
- Data Description
  - Project uses "ingredient_and_quantity.json" for training a CRF model to extract ingredients, quantities and units from recipes
- Data Ingestion & Preparation
  - Read Recipe Data & Preparation
     - Define a "load_json_to_dataframe" function to read data from a JSON file
     - Execute the load_json_to_dataframe function
     - Describe the DF, print first 5 rows, dimensions and information
  - Recipe Data Manipulation
     - Create "input_tokens" and "pos_tokens" columns by splitting data
     - Validate length equality of "input_tokens" and "pos_tokens"
     - Define & execute a "unique_labels" function
     - Provide insights and identify indexes requiring cleaning
     - Drop rows with invalid data
     - Update & validate "input_length" and "pos_length"
- Train Validation Splot (70 train- 30 val)
  - Splitting the dataset
     - Split the dataset into training and validation sets with a 70:30 ratio
     - Print the first 5 rows of both training & validation DFs
     - Extract data into "X_train", "X_val", "y_train", "y_val"
     - Display the number of unique labels present in "y_train"
- Exploratory Recipe Data Analysis on Training Dataset
 - Data flattening & Token extraction
     - Define a "flatten_list" function and initialise the dataset name
     - Define and execute an "extract_and_validate_tokens" function
  - Token categorisation & Frequency analysis
     - Define and execute a "categorize_tokens" functions
     - Define and execute a "get_top_frequent_items" function for ingredients and units
  - Visualisation & Insights
     - Define a "plot_top_items" function
     - Plot bar graphs for top ingredients and units in the training dataset
     - Provide insights based on the visualisation
- Conclusion
  - Recommendations to track and compare market capitalisation of the top global banks to evaluate competitiveness and dominance
  - Suggestions to use cross-currency analysis (USD, GBP, EUR, INR) for consistent benchmarking of financial institutions across regions
  - Propose continuous monitoring of market share concentration to identify growth opportunities for mid-tier banks
  - Identify potential regions or banking segments for expansion by analysing gaps between tiers of banks and regional trends

Python libraries used:
- sklearn-crfsuite==0.5.0
- spacy==3.5.3
- pandas==2.2.2
- matplotlib==3.10.0
