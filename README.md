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

order_id,customer_id,order_status,order_purchase_timestamp,order_approved_at,order_delivered_carrier_date,order_delivered_customer_date,order_estimated_delivery_date  
100,ascd534,delivered, 2017-10-02 10:56:00.000,	2017-10-02 11:07:00.000, 2017-10-04 19:55:00.000, 2017-10-10 21:25:00.000,2017-10-18 00:00:00.000


## Target Table

```sql
CREATE TABLE CustOrders(
    [order_id] varchar(200)
      ,[customer_id] varchar(200)
      ,[order_status] varchar(200)
      ,[order_purchase_timestamp] 
      ,[order_approved_at] datetime
      ,[order_delivered_carrier_date] datetime
      ,[order_delivered_customer_date] datetime
      ,[order_estimated_delivery_date] datetime 
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
