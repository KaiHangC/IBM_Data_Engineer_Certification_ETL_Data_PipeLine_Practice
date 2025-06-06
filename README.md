# IBM_Data_Engineer_Certification_ETL_Data_PipeLine_Practice
This project is an ETL data pipeline build with Python. 

The data source is provided by [IBM](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0221EN-SkillsNetwork/labs/module%206/Lab%20-%20Extract%20Transform%20Load/data/datasource.zip)

This project demonstrates a simple ETL (Extract, Transform, Load) pipeline implementation that processes vehicle data from multiple file formats (CSV, JSON, and XML) and outputs the transformed data to a unified CSV file.

## Features
Data Extraction: Reads data from three different file formats:
- CSV (data.csv)
- JSON (data.json)
- XML (data.xml)

Data Transformation:
- Standardizes data structure across all sources
- Rounds price values to 2 decimal places
- Handles potential data inconsistencies

Data Loading:
- Writes transformed data to transformed_data.csv
- Maintains all original columns: 'car_model', 'year_of_manufacture', 'price', 'fuel'

Logging:
- Tracks all major operations
- Records errors and warnings
- Saves logs to log_file.txt

## File Structure
```
/home/project/data_source/
│── etl_practice.py        # Main ETL script
│── data.csv               # Sample CSV data provided in the link
│── data.json              # Sample JSON data provided in the link
│── data.xml               # Sample XML data provided in the link
│── transformed_data.csv   # Output file after transformation
│── log_file.txt           # Logs of ETL operations
```

## Data Schema
All input files should contain the following fields:
- car_model: String (Name of the car model)
- year_of_manufacture: Integer (Manufacturing year)
- price: Float (Vehicle price, will be rounded to 2 decimal places)
- fuel: String (Fuel type: Petrol/Diesel/Electric/etc.)

## Usage
- Place your source data files (CSV, JSON, XML) in the project directory
- Run the ETL script:
```
python etl_practice.py
```
- Check the output:
  - Transformed data: transformed_data.csv
  - Process logs: log_file.txt

## Dependencies
- Python 3.x
- Python libraries:
  - pandas
  - glop
  - xml.etree.ElementTree
