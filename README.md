# Signaling-Data-ETL
### Overview
This project focuses on building a robust ETL (Extract, Transform, Load) pipeline using SQL Server Integration Services (SSIS) to process and audit signaling data generated by network subscribers. The ETL pipeline is designed to handle large volumes of data efficiently, apply error-handling techniques, and maintain a detailed audit trail for data processing.

## Project Structure
### ETL Pipeline
- Source Data: Subscriber signaling data, including activities like calls, browsing, and SMS, collected by the network vendor in real-time and in bulk.
- Processing: The pipeline processes dumped files, handles errors, and maintains an audit of processed records.
![صورة واتساب بتاريخ 2024-08-12 في 18 10 52_973a4135](https://github.com/user-attachments/assets/9a390961-dc15-4fcc-b895-a5b2badb9e1e)
![صورة واتساب بتاريخ 2024-08-12 في 18 10 57_6fee34ea](https://github.com/user-attachments/assets/f16891ef-dbb9-4b87-a8ec-05a3da7682b9)

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

