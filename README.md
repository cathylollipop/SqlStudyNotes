# SqlStudyNotes

## Database Design
#### Some Concepts
* Relation : connections between data
* Entity : anything that we store information about. eg.Calab, Bill
* Entity type : categories of entities. eg.user
* Attribute : things we store
* Attribute typse : categories of attributes. eg. name, username, password
* Attribute values : eg.Calab, CalabCurry, pass123
* Database Management System (DBMS) : allows us easily manipulate with and manage data
* RDBMS : design to work with relational database, eg. MySQL, SQL, Oracle
* allows us to change the data is presented -> veiw mechanism -> giving different views -> security feature
* front end is consistency
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
