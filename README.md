# Signaling-Data-ETL
### Overview
This project focuses on building a robust ETL (Extract, Transform, Load) pipeline using SQL Server Integration Services (SSIS) to process and audit signaling data generated by network subscribers. The ETL pipeline is designed to handle large volumes of data efficiently, apply error-handling techniques, and maintain a detailed audit trail for data processing.

## Project Structure
### ETL Pipeline
- Source Data: Subscriber signaling data, including activities like calls, browsing, and SMS, collected by the network vendor in real-time and in bulk.
- Processing: The pipeline processes dumped files, handles errors, and maintains an audit of processed records.
![flow](https://github.com/user-attachments/assets/30fd5430-097e-44ac-8be2-bcfdde2bc320)
![dft](https://github.com/user-attachments/assets/70570ddd-6c44-4ac4-a180-afc0fc1e4536)


### Audit Table
dim_audit: Captures the number of rows extracted, inserted, and rejected for each file, offering a comprehensive overview of the ETL process.
### Error Handling
- Implemented various error-handling techniques to manage:
  - Null values in non-nullable attributes.
  - Data type mismatches.
  - Incomplete records.
## Technical Details
- Source Systems: Flat files are dynamically processed through the Foreach Loop container.
- Variables: Used to dynamically adjust source system paths.
- Audit Mechanism: Tracks key metrics like rows processed and records errors to ensure data quality.
## Usage
To use this project, follow these steps:

1- Clone the repository to your local machine.
2- Open the SSIS project in Visual Studio.
3- Configure the connection managers to point to your source systems.
4- Run the ETL packages to load and audit the signaling data.
License
License: MIT

## Acknowledgments:
This is one of Garage Education's use cases, and I used Et3lm Online's implementation as a reference.
This project was developed using SQL Server Integration Services (SSIS).

