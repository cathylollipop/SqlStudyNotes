# SqlStudyNotes

## Database Design
#### Some Concepts
* Entity : anything that we store information / data about. eg.Calab, Bill
* Entity type : categories of entities. eg.user
* Attribute : things we store
* Attribute typse : categories of attributes. eg. name, username, password
* Attribute values : eg.Calab, CalabCurry, pass123
* Relation : connections between two sets of data -> another name of a table -> different sets of data
* Table : physical representation of relation
* Rows : specific entries
* Tuple : another thing of row -> all the attributes about a specific entity -> a row on a table
* Columns : specific attribute
* Other: File(table) Record(row) Field(column) 
* Value : the specific information we put in to a specific column 
* Entry : a row
* Schema : drawn out structure of our database
* Database Management System (DBMS) : allows us easily manipulate with and manage data
* RDBMS : design to work with relational database, eg. MySQL, SQL, Oracle
* allows us to change the data is presented -> veiw mechanism -> giving different views -> security feature
* front end is consistency
* Null : when someone doesn't enter a value on a column of a table -> empty value, no value, no data
* Anomalies : error within our data integrity, go away from normal
* Integrity : implmente integrity to protect agains anomalies
* Normalization : the process of building best database design
* Keys
#### SQL
* a programming language used to communicate to a database -> mediator btw computer, database and human
* 2 main categories:
* SQL defines the database structure - Data Definition Language (DDL) eg. CREATE
* SQL manipulates the data within - Data Manipulation Language (DML) eg. UPDATE
* Naming Conventions
#### Database Design
* Data Integrity : all data is correct, up to date, managed properly, no repeating data
* 3 sections:
* Conceptual Schema : how things / data are related, general ideas
* Logical Schema : start to plan out table structure
* Physical Schema : specific, actually implementing database, what server, how to get access to our data
#### Data Integrity
* Entity Integrity : having uniqueness among entities -> unique entities, id -> uniqueness of entities
* Referential Integrity : when we reference the id of a table with another table, keys across multiple table
* Domain Integrity : the range of values that are accepatable for a column, eg. phone should be a 10-digit number
* Data Type : Numbers, Text, Dates -> can put limits on the data we want to store, eg. char(20)
* Foreign key constraints



## Oracle Database
Enterprise database
#### Database Design - Entities & Attributes 
* Entities (generic & specific)
* Attributes describe something (generic attributes describes generic entity, specific attributes describe specific entity)
* In a table: Entity type (Customer), Attribute Types (Name, Phone#, height, birthday), Specific Entity (each row), Specific Attributes (Superman, 1800-999-9999, 7'11'', 06/09/1938)
* protect integrity of our database -> connections between tables / relationship

#### Languages
* SQL : Structured Query Language. Human readable -> SQL -> machine code
* RDBMS : Relational Dabatase Management System
* Relational : Relations -> describe talbes (col & row). relations = tables
* Relationship: connections between tables
* Null : absence of a value, if some row has no value, it's null -> to represent the lack of value
* Primary key : usually a random generated number -> id -> prevent duplicate data.
* Foreign key
* Constraint : to protect the primary key, foreign key, and relationships
* Indexes : allows the database to find the information faster -> primary keys will get the indexes automatically
* Data type
