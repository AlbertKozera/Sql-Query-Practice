# SQL Query Practice - City Buses

## Overview

This project is designed to analyze data related to public city bus transportation. The database allows us to gather insights from individual bus trips. 
The database consists of 12 tables, which are loaded and managed using a custom data generator and SQL loader scripts.

## Database Schema

![image](https://github.com/user-attachments/assets/e500f550-4fd3-4247-9fe1-6dee70ff1cfd)

The database schema includes the following tables:

- `Przejazd` (Trip)
- `Osoba` (Person)
- `Rozkład` (Schedule)
- `Firma` (Company)
- `Pojazdy` (Vehicles)
- `Linia` (Line)
- `Pracownik` (Employee)
- `Miasto` (City)
- `Czas` (Time)
- `Dzień` (Day)
- `Miesiąc` (Month)
- `Rok` (Year)

## Data Loading Process

Data was generated using a custom-built Java generator with several validations (e.g., unique IDs, correct order of months). The following records were generated and stored in CSV files:

- `Przejazd` - 5000 records
- `Osoba` - 500 records
- `Rozkład` - 500 records
- `Firma` - 500 records
- `Pojazdy` - 500 records
- `Linia` - 500 records
- `Pracownik` - 500 records
- `Miasto` - 500 records
- `Czas` - 500 records
- `Dzień` - 31 records
- `Miesiąc` - 12 records
- `Rok` - 4 records

Data is loaded into the database using the `sqlldr` (SQL Loader) script.

## Analytical Queries

### Rollup Queries
- Number of discounted tickets validated per day, per line
- Kilometers covered in each trip

### Cube Queries
- Salaries of public transport employees
- Number of stops a line passes through

### Partition Queries
- Percentage of lines operating on specific dates
- Percentage of vehicles operating on specific lines

### Grouping Sets Queries
- Total revenue for each trip
- Kilometers covered by specific vehicles on certain routes

### Window Queries
- Average trip duration for 2017-2018
- Average kilometers per trip for 2015-2017
