# ETL_EXTRACT_SUSANOTIENO
Susan Otieno
## Description

This project contains a Jupyter notebook (`etl_extraction.ipynb`) that demonstrates an ETL (Extract, Transform, Load) process on student data. The notebook reads a CSV file (`custom_data.csv`), processes and analyzes the data, and supports both full and incremental extraction based on a checkpoint file (`last_extraction.txt`).

##  Tools Used

- Python
- pandas
- Jupyter Notebook
  
##  Install Requirements  
   Make sure you have Python and Jupyter installed. Install pandas if needed:
   
   pip install pandas
   

##  Data Source 
   The data is provided in `custom_data.csv` in the project directory.

##  Run the Notebook  
   Open `etl_extraction.ipynb` in Jupyter Notebook or JupyterLab and run all cells.

##  Incremental Extraction 
   The notebook uses `last_extraction.txt` to track the last extraction time. To reset or change the checkpoint, edit this file.

##  Transformations Applied

Filled missing values in `parental_education_level` with 'Unknown'
Categorized `age` into groups: Teen, Young Adult, Adult
Classified `exam_score` as Pass/Fail

##  Loading Method Used
Transformed CSV files are loaded into SQLite databases using pandas and sqlite3.
##  Sample code
# Load the full transformed CSV into a DataFrame
df_full = pd.read_csv(full_csv)
# Save to SQLite database
conn_full = sqlite3.connect(full_db)
df_full.to_sql('full_data', conn_full, if_exists='replace', index=False)
conn_full.close()

## Output Location
SQLite databases are stored in the `loaded_data` directory
