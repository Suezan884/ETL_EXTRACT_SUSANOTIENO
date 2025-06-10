# ETL_EXTRACT_SUSANOTIENO
Susan Otieno
## Description

This project contains a Jupyter notebook (`etl_extraction.ipynb`) that demonstrates an ETL (Extract, Transform, Load) process on student data. The notebook reads a CSV file (`custom_data.csv`), processes and analyzes the data, and supports both full and incremental extraction based on a checkpoint file (`last_extraction.txt`).

#  Tools Used

- Python
- pandas
- Jupyter Notebook
  
#  Install Requirements  
   Make sure you have Python and Jupyter installed. Install pandas if needed:
   
   pip install pandas
   

2. #  Data Source 
   The data is provided in `custom_data.csv` in the project directory.

3. #  Run the Notebook  
   Open `etl_extraction.ipynb` in Jupyter Notebook or JupyterLab and run all cells.

4. #  Incremental Extraction 
   The notebook uses `last_extraction.txt` to track the last extraction time. To reset or change the checkpoint, edit this file.
