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
* Frontend - user see - access data in certain ways - view system
* Backend - what's going on behind the scenens - server side code
* front end is consistency
* Client Side : accessing the database
* Server Side : serves instances of the database to clients
* Server Side Scripting Language 
* Views : taking the data from database and illustrate in different ways
* Joins
* Null : when someone doesn't enter a value on a column of a table -> empty value, no value, no data
* Anomalies : error within our data integrity, go away from normal
* Integrity : implmente integrity to protect agains anomalies
* Normalization : the process of building best database design
* Keys
#### SQL
* structured query language - a programming language used to communicate to a database -> mediator btw computer, database and human
* 2 main categories:
* SQL defines the database structure - Data Definition Language (DDL) eg. CREATE
* SQL manipulates the data within, update delete search values - Data Manipulation Language (DML) eg. UPDATE
* Naming Conventions
* SQL keywords : SELECT ...
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
#### Atomic Value
* The value stores in a column is one thing, smallest one individual thing stored
* Break it down and treat it as one thing. Eg. first name, middle name, last name -> not single letters
* Not to store multiple things in a column -> singlular
#### Relationships
* In a database, everything is connected, rather than storing everything in a giant table, split it out, break into multiple tables
* Relationships talk about entities, they are related in some way, there is a relationship btw them
* One-to-One Relationships : one entity has connection to another one entity. eg.marriage, SSN
* One-to-Many Relationships : one entity can have a relationship to multiple other entities, but a specific entity can only be related back to the one entity. eg.comment on a youtube video -> a user can have many comments, but one comment is owned by one user
* Many-to-Many Relationships : eg. class vs student -> multiple students can in one class, a class can have multiple students; a student can take multiple classes, multiple classes can be taken by same student
* Parent Tables and Child Tables : primary key (parent), foreign key (child)
#### Design One-to-One Relationships
* one table : eg. username is exclusive to an account -> put username as an attribute of user. no other info about username needs to be stored, store username as a column
* multiple tables : when we want to add extra attributes to 1:1 attribute. eg. 1 cardholder : 1 card -> cardholder table, card table -> cardId as reference in cardholder table
* 1:1 relationship : use as an attribute or another table,
#### Design One-to-Many Relationships
* two tables : eg. one user can have multiple credit cards, but one card can only be owned by one user. -> put userId in the card table. -> many side gets a foreign key pointing to the one side.
* Foreign key : id connection, foreign key points to the primay key in the primay table -> parent-child relationship, child has to point to parent.

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
