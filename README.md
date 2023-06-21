# sql-challenge


This assignment using SQL required us to work as data engineers with employee datasets, contained in 6 CSVs.  We were required to create a diagram, a schema, and 8 queries to get answers for the fictional company.

Our first piece was data modeling and required us to create a Entity Relationship Diagram of the 6 CSV tables.  The diagram was created, notating the primary keys (or composite keys for dept_manager and for the demp_emp tables), and the cardinality of the relationships.  I took a snip of the diagram and saved it as a PNG file, and also exported the schema.  I saved this file as ‘schema from quickdatabase_diagram’.  

I used this as a guideline in creating my schema for the assignment.  I wanted it to be a little cleaner.  There is a DROP TABLE in a specific order (as it would not drop certain tables before other due to constraints/foreign keys).  The first table was ‘titles’ with a primary key set and both set as NOT NULL VARCHARS.  

Next was ‘employees’.  All are set as NOT NULL except birth_date as it is not needed for queries and not a foreign key.  I initially set birth_date as a date, but it would not import the table as a date and gave me an error on the format.  Because there is no analysis or queries that need the birth_date as a date, I assigned it as a VARCHAR.  I did not have issues with hire_date coming in as date.  I learned that PG Admin likes the dates as ‘YYYY-MM-DD’ and the hire_date is that format.

‘Departments’ was next with both as NOT NULL and VARCHAR format.  A primary key was defined.
‘dept_emp’ was next with the emp_no as an integer and the dept_no as a VARCHAR.  This has a composite key as neither column is unique.
‘dept_manager’ is also a composite key so neither column can be NULL. 
Last was ‘salaries’.  Both columns were integers and neither can be NULL.
 Once this schema was run, the tables were imported but had to be in a specific order because of constraints/foreign keys.  In order to avoid constraint violations, the tables need to be imported in the following order:
Departments, Titles, Employees, Dept_Emp, Dept_Manager, and Salaries.

Once the tables are imported, the queries can be run.  
The queries often required inner joins to combine columns from multiple tables.  

This homework was completed with the help of a study group and class examples and a few internet searches to help understand SQL.

