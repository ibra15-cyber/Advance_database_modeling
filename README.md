# DCIT 404 Advanced Database Final Project

This repository contains the final semester project for the DCIT 404 - Advanced Database course. It involves designing and implementing a comprehensive database system that adheres to the principles of data normalization and integrity. The project showcases the practical application of database management concepts, including the creation of Entity-Relationship (E-R) diagrams, normalized tables, and SQL commands to manage relationships and constraints.

## Authors

- Ibrahim Anyars Safianu – 10826754  
- Todd Nelson – 10821793  
- Claudia Fiadonu – 10838276  
- Stephen Essien Mensah – 10829102  
- Daniel Kissi – 10854734  

---

## Table of Contents

1. [Entities and Attributes](#entities-and-attributes)  
2. [Key Fields and Integrity Constraints](#key-fields-and-integrity-constraints)  
3. [Normalized Tables](#normalized-tables)  
4. [E-R Diagram](#e-r-diagram)  
5. [SQL Table Creation with Cascading Actions](#sql-table-creation)  

---

## Entities and Attributes

The project identifies and defines key entities such as:  
- Supervisor, Enumerator, Region, District, Sub-District, Locality  
- Household, Household Status, Usual Household Members, Visitors, Absent Members, Emigrants  
- Economic Activity, Disability, ICT, Fertility, Mortality, Agriculture, and Housing Condition  

Each entity includes detailed attributes, such as primary keys, foreign keys, and associated constraints.  

---

## Key Fields and Integrity Constraints

All tables include:  
- **Primary Keys** for unique identification.  
- **Foreign Keys** to establish relationships between tables.  
- **Constraints** such as `NOT NULL`, `CHECK`, `UNIQUE`, `ON DELETE CASCADE`, and `ON UPDATE CASCADE` to ensure data integrity.  

---

## Normalized Tables

The database adheres to the principles of:  
- **1NF**: Eliminates duplicate data and organizes attributes into unique rows and columns.  
- **2NF**: Breaks down tables into parent-child relationships, ensuring no partial dependencies.  
- **3NF**: Removes calculated fields, ensuring all non-key attributes depend only on the primary key.  

---

## E-R Diagram

The E-R Diagram visually represents the relationships between entities and provides a clear overview of the database structure.

---

## SQL Table Creation

The project includes SQL commands to create the following:  
- **Parent Tables**: Supervisor, Region, Household, etc.  
- **Child Tables**: Usual Household Members, Visitors, Absent Members, etc.  
- **Cascading Actions**: Implements `ON DELETE CASCADE` and `ON UPDATE CASCADE` to maintain referential integrity.  

Sample Table:  
```sql
CREATE TABLE Household (
    HouseholdID INT PRIMARY KEY,
    EnumerationAreaID INT,
    RegionID INT,
    DistrictID INT,
    SubDistrictID INT,
    LocalityID INT,
    StreetAddress VARCHAR(255),
    HouseCompoundGroupQuartersDescription VARCHAR(255),
    FOREIGN KEY (RegionID) REFERENCES Region(RegionID) 
      ON DELETE CASCADE ON UPDATE CASCADE
);
```

---

## Key Features

- Comprehensive database design and implementation.  
- Detailed documentation of attributes and constraints.  
- Practical application of normalization principles.  
- Dynamic SQL scripts for creating and managing database tables.  

---

## License

This project is licensed under the [MIT License](LICENSE).  

--- 

## How to Use

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/dcit404-database-project.git
   ```
2. Execute the SQL scripts using Oracle SQL Developer or any preferred database management tool.  
3. Modify and adapt the database structure as needed for your use case.  

