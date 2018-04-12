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
* binary relationships
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
* child has the foreign key pointing back to the parent
#### Design Many-to-Many Relationships
* the two many sides are both parents
* break up into two one-to-many relationships and an intermediary table (3 tables)
* eg. classes & students -> need an intermediary / junction table -> how we connect our tables
* intermediary becomes the child point to both parents
* class table (1) : id(primary key)
* intermediary table (many) allows one table talks to another table : class_id student_id -> foreign keys
* students table (1) : id(primary key)
* ![image](https://user-images.githubusercontent.com/20292261/38683405-fa29b7f6-3e32-11e8-9d38-d8ce88b3735d.png)
#### Keys
* should always be unique : eg. natural key - what already in the table, no need to create new key, eg. username
* key should never be changing
* never Null 
#### Index
* we order the data that database can understand how to find data
* key is a type of index
#### Look up tables
* ids help create better connections between tables requiring less maintainance for our database and also protect our integrity -> don't need to worry about incorrect values in "many" side tables, just need to update one row in "1" side
* foreign key constraints
* what do keys do for us? 
* Protect our integrity - only update some value, less maintainance, less incorrectness
* Make things unique
* Improves speed, improves functionality of our database
* Make updating easier - less work
* Allows for added complexity - add new column 
#### Superkey & Candidate Key
* superkey : any number of columns that forces every row to be unique, superkey is usually not defined in db table, each row is unique. superkey is for designing database only, not practical. superkey is asking : Can every row be unique always? 
* candidate key : the least number of columns, eg. the username is unique and enough to make each row unique. candidate key is asking : How many columns are needed? 
* How many candidate keys do I have? we can have more than one candidate key. eg. username and email can be two candidate keys. Once we figure out all candidate keys, we decide primary key.
#### Primary key
* A list of possiblities of candidate keys eg. username, email, first name + last name + address + birthday...
* pick primary key from above list based on rules (unique, never change, never Null), eg. username
* create index for primary key
#### Alternate Key
* All the candidate keys that are not selected as primary key
* it's also useful to create index for alternate keys
#### Surrogate Key & Natural Key
* more for database design
* Surrogate Key : made up keys, added to your database no matter what, give an id for every single row. kept completely private. eg. user_id - random number, no real world meaning. student_id actually has real world meaning, not good choice for surrogate keys.
* Natural Key : something that's naturally already in the table, they have real-world value. You always want to try to make things unique naturally.
* pros of natural keys : already defined you don't need to create or define new data, smaller database
* cons of natural keys : sometimes it's hard to find a good natural key that fits 3 key rules; natural keys have real world meaning, you have connections to real world meaning, if real world changes natural keys will change
* pros of surrogate key : they are typically numbers, usually easy to work with
* cons of surrogate key : you have to add a column to your table no matter what, requires you to store more data, it can be confused sometime
#### Foreign Keys
* a reference that references primary key in the same or separate table
* what keeps things connected
* you can have only one primary key but you can have multiple columns having foreign key relations to different tables but each column can only have one reference 
* NOT NULL : you have to give a value - you are eliminating all rows that arent' have a value, you are preventing that from happening
* NOT NULL foreign key : what is required? relationship
* We can't have the primary key values to be changed, but we can have the foreign key reference to be changed because reference changes
* primary key is NEVER NULL, but foreign key is not always required to have a connection to primary key, the connection is optional
* NOT NULL forces the relationship to be there




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


Reference: https://www.youtube.com/channel/UCZUyPT9DkJWmS_DzdOi7RIA
