# SSIS ETL Project - CSV to SQL Server

## Project Overview

This project demonstrates an ETL pipeline built using SQL Server Integration Services (SSIS).

The pipeline performs:

1. Truncate staging table
2. Read customer data from CSV file
3. Load data into SQL Server table
4. Validate records
5. Store cleaned data

## Technologies Used

- SSIS
- SQL Server
- Visual Studio
- GitHub

## Source Data

CSV File:

customer_id,customer_name,city
1,Ram,Hyderabad
2,Sita,Delhi

## Target Table

```sql
CREATE TABLE Customers(
    customer_id INT,
    customer_name VARCHAR(100),
    city VARCHAR(100)
);
```

## Package Flow

Control Flow:

Truncate Table
↓
Load CSV Data

Data Flow:

CSV Source
↓
OLE DB Destination

## How to Run

1. Open project in Visual Studio
2. Open Demopackage.dtsx
3. Update SQL Server connection
4. Execute package

## Future Improvements

- Data validation
- Lookup transformations
- Error handling
- Multiple file processing
