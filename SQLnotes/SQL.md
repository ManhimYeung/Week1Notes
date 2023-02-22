# SQL Notes

### Relational Database

##### What is it?

A relational database is a collection of data items with pre-defined relationships between them. 
These items are organised as a set of tables with columns and rows. 
Tables are used to hold information about the objects to be represented in the database.

##### Primary Keys

* Identifies each record
* Must contain __UNIQUE__ values 
* Cannot be empty
* Cannot be changeable
* Can be a single column(Simple)
* Can be multiple columns(Composite)
* Only one primary key per table!!!
* [How to use Primary Keys in SQL](#Using-Primary-Keys) 

__Example for simple column__

ID|Name|Gender
-----|-----|-----
1001|Chris|Male
1002|John|Male
1003|Ellie|Female
1004|Maria|Female

__Example for multiple columns__

Order No. |Line No. |Product Code |Quantity
-----|-----|-----|-----
10667|1|SCREW083|150
10667|2|NUT392|32
10667|3|BOLT283|32
10668|1|NUT392|180
10669|1|SPANN920|2
10669|2|WRENCH932|1

##### Foreign Keys

* Reference Primary Keys of other tables
* A table can have more than 1 Foreign Keys
* Values do not have to be unique
* The RDBMS(Relational database management system) will prevent any changes that violate the relationship constraints
* [How to use Foreign Keys in SQL](#Using-Foreign-Keys)

__Example for Foreign Keys__

![Image1](https://cdn.discordapp.com/attachments/955109188609114135/1077973644145328208/image.png)

Using __Authors ID__ and __Publisher ID__ as foreign keys to replace __Authors Name__ and __Publishers Name__.

![Image2](https://cdn.discordapp.com/attachments/955109188609114135/1077974476437848125/image.png)

### Data Modelling

##### What is it?

Data modelling is the process of diagramming data flows. When creating a new or alternate database structure, 
the designer starts with a diagram of how data will flow into and out of the database.

* Detail how information is organised
* Show relationships between table
* Three levels:
  1. [Conceptual](#Conceptual-Data-Model) (broad level business understanding of data structure)
  2. [Logical](#Logical-Data-Model) (defines data structure elements and relationships between them independent of the database management system)
  3. [Physical](#Physical-Data-Model) (details the specific implementation of the model dependent on the RDBMS being used)
* Reflect real-world relationships

##### Conceptual Data Model

* Entity Names
* Entity Relationships
* Store data on separate tables

![Image3](https://cdn.discordapp.com/attachments/955109188609114135/1077983010378489936/image.png)

##### Logical Data Model

* Entity Names
* Entity Relationships
* Attributes
* Primary Keys (labeled as PK image below)
* Foreign Keys (labeled as FK image below)

![Image4](https://cdn.discordapp.com/attachments/955109188609114135/1077983787947937852/image.png)

##### Physical Data Model

* Primary Keys
* Foreign Keys
* Tables Names
* Column Names
* Column Data Types

![Image5](https://cdn.discordapp.com/attachments/955109188609114135/1077984437029052466/image.png)

##### Types of Relationship

* one to one
* one to many
* many to many

### ERDs (Entity Relationship Diagrams)

##### What does ERD do?

* Represents all entities in data models
* Each entity represented by a table in the database
* Each entity has attributes
* Use Crow's Foot Notation([Examples](#Crow's-Foot-Notations)) to describe relationships in detail

##### Crows's Foot Notations

* one(Author) to(direction arrow) many(Books)
![Image6](https://cdn.discordapp.com/attachments/955109188609114135/1077986590711889970/image.png)

* Other examples below
![Image7](https://cdn.discordapp.com/attachments/955109188609114135/1077987330486435920/image.png)
![Image8](https://cdn.discordapp.com/attachments/955109188609114135/1077987469179506740/image.png)

### Normalisation and Normal Forms

##### What is Normalisation?
Normalisation is the process that separate the table out into separate tables.

__Pros:__
* Reduces data redundancy
    1. Eliminates repeated information
* Increases ease of database maintenance
    1. One source of truth for each entry
    2. Easier inserts
    3. Easier updates
    4. Easier deletes

__Cons:__
* Increases database depth (more tables)
* Increases difficulty of querying
    1. More effort for analysts/devs
    2. More computational effort
    
##### Normal Forms

###### First Normal Form(1NF)
* Data must be atomic
* No repeated groups
* Each row must be unique

Starting with the first normal form:

![Image9](https://cdn.discordapp.com/attachments/955109188609114135/1077991124955844719/image.png)
Spartan Column: Name and Rank can be separated.
![Image10](https://cdn.discordapp.com/attachments/955109188609114135/1077991706655457341/image.png)
Weapons Column: Can have multiple columns to show different type of weapons.
![Image11](https://cdn.discordapp.com/attachments/955109188609114135/1077992240456138772/image.png)
Weapons Column: Repeated groups of weapons, therefore separate weapon information into another table.
![Image12](https://cdn.discordapp.com/attachments/955109188609114135/1077993013084704878/image.png)
Weapons Column: Weapon Smith and Location have to be separated.
![Image13](https://cdn.discordapp.com/attachments/955109188609114135/1077994317722959922/image.png)
Assign primary key so that each row is unique, and then use it as a foreign key on second table.
![Image14](https://cdn.discordapp.com/attachments/955109188609114135/1077995168797569074/image.png)

###### Second Normal Form(2NF)
* Meets all requirements in [First Normal Form](#First-Normal-Form(1NF))
* All non-key attributes must functionally depend upon the full primary key

Using the second table from 1NF:
![Image15](https://cdn.discordapp.com/attachments/955109188609114135/1077996503211196556/image.png)
Spartan ID and Weapon Names have repeated values, so combine both of them to make a new primary key.
![Image16](https://cdn.discordapp.com/attachments/955109188609114135/1077997714220007587/image.png)
Now that weapons are made by the specific smith, but this information does not stay forever.
So now assign a weapon ID to the tables.
![Image17](https://cdn.discordapp.com/attachments/955109188609114135/1077998425523638332/image.png)
Meets the requirements of both 1NF and 2NF.

###### Third Normal Form(3NF)
* Meets all requirements in [Second Normal Form](#Second-Normal-Form(2NF))
* There are no transitive dependencies

Using the 3 tables from 2NF:

![Image18](https://cdn.discordapp.com/attachments/955109188609114135/1077999381946572851/image.png)
The Name and DOB are independent upon the ID of the spartan. Checked :)
![Image19](https://cdn.discordapp.com/attachments/955109188609114135/1077999868351631440/image.png)

Primary key is a combination of both columns. Checked :)
![Image20](https://cdn.discordapp.com/attachments/955109188609114135/1078000349832548372/image.png)
Weapon and Weapon smith depend on Weapon ID but Smithy Location does not depend on Weapon ID.
So Assign a new ID for weapon Smith.
![Image21](https://cdn.discordapp.com/attachments/955109188609114135/1078001812147281961/image.png)
Now the table is normalised in 3NF. Checked :)


### SQL Database & Tables Command
1. Create database
```SQL
CREATE DATABASE Database_name --use "_" of " ", otherwise eg. [sparta demo]
```

2. Create table:
```SQL
CREATE TABLE table_name (
    column1_name data_type,
    column2_name data_type
);
```

3. Drop table:
```SQL
DROP TABLE table_name; --Delete the table
DROP TABLE IF EXISTS table_name; --Delete the table if it exists
```


### Data Types
```SQL
name VARCHAR(20), --takes 20 char's
notes VARCHAR(max), --takes maximum char's allowed by the SQL server
phone_number CHAR(11), --takes a fixed number of char's
birthdate DATE, --stored as date
first_shift_start, DATETIME --stored as date and time
lunch_break, --stored as time
balance INT, --stored as integers
rate DECIMAL(4,2), --(precision, scale) eg.32.15 4 digits total, 2 after decimal
height_metres FLOAT(24), --stored as large digits eg. 3.45e11
is_full_time BIT --stored as bool 1 or 0
```
Extra note: 

__NULL__
* missing or unknown value
* it is not a value
* NULL =/ NULL

### Insert Data
```SQL
--Using the data types above as exmaple
INSERT INTO table_name (
    name, notes, phone_number, birthdate,
    first_shift_start, lunch_break, balance,
    rate, height_metres, is_full_time

) VALUES (
    'Manhim', --name
    'A random spartan from Sparta', --note
    '07123456789', --phone
    
    --american style for date, datetime and time
    '1995-03-06', --birthdate
    '2023-02-22 09:30:00', --first_shift_start
    '12:30:00', --lunch_break
    
    --no quotes for numbers
    5, --balance
    12.32, --rate
    1.77e1, --height_metres
    
    1 --is_full_time 
);
```

### Insert more than one instance of data
```SQL
DROP TABLE IF EXISTS films

CREATE TABLE films (
    film_title VARCHAR(180)_,
    release_date DATE,
    box_office_gbp DECIMAL(10, 0),
    runtime_mins INT,
    is_oscar_winning BIT
);
/*
INSERT INTO films (
    film_title, release date, box_office_gbp, runtime_mins, is_oscar_winning
) VALUES 
('Neighbours Wife', '2023-02-22', 96843861, 1),
('High School Teacher', '2023-02-22', 456463, 0);
*/

INSERT INTO films (
release_date, is_oscar_winning, film_title)
VALUES (
'2020-07-02', 0, 'Best mother in the world'); 
--box_office_gbp and runtime_mins would be declared as NULL
```

### Constraints
```SQL
DROP TABLE IF EXISTS films

CREATE TABLE films (
    film_title VARCHAR(180)_,
    release_date DATE,
    box_office_gbp DECIMAL(10, 0),
    runtime_mins INT,
    is_oscar_winning BIT --DEFAULT 0 sets default value to 0
);

INSERT INTO films 
(film_title, release_date) --(release_date) has error because title is VARCHAR not NULL
VALUES 
(NULL, '2001-06-29'); 
--error because title is a VARCHAR not NULL
```

### Using Primary Keys
```SQL
DROP TABLE IF EXISTS course;
CREATE TABLE course(
    course_id INT PRIMARY KEY, --sets course id to be a column that takes unique integer
    course_name VARCHAR(20) UNIQUE --course name now must be unique
);

INSERT INTO course
(course_id, course_name)
VALUES
(1, 'CSharp');
(2, 'CPlusPlus')
(3, 'JavaScript');
--(1, 'Java'); error because course id duplicated
--(NULL, 'Java'); error because course id is not NULL
--(4, 'CSharp'); error because course name must be unique
```

```SQL
DROP TABLE IF EXISTS course;
CREATE TABLE course (
    course_id INT PRIMARY KEY IDENTITY(1,1), IDENTITY --starts at 1 then
                                                      --increment by 1 each time
    course_name VARCHAR(20) UNIQUE --course name now must be unique
);

INSERT INTO course
(course_name)
VALUES
('CSharp'),
('CPlusPlus'),
('JavaScript');
```

### Using Foreign Keys
```SQL
DROP TABLE IF EXISTS students;

CREATE TABLE students (
    student_id INT PRIMARY KEY IDENTITY(1,1),
    student_name VARCHAR(20),
    course_id INT FOREIGN KEY REFERENCES courses (course_id) 
    --course table from primary key section
);
INSERT INTO students
(student_name, course_id)
VALUES 
('Alice', 1),
('Bob', 1),
('Charlie', 2)
('David', 5); --error beccause course id must be 5 doesn't exist from previous table

DROP TABLE courses; --error because student table takes course_id
```

### Updating Table
```SQL
ALTER TABLE films
ADD budget DECIMAL(10,0), synopsis VARCHAR(200); --Add new columns to the table

ALTER TABLE films
ALTER COLUMN runtime_mins DECIMAL(5,2); --Change runtime_mins data type

ALTER TABLE films
DROP COLUMN box_office_gbp; --Remove box_office_gbp from the table
```

```SQL
CREATE TABLE ice_cream (
    id INT,
    flavour VARCHAR(20),
    price DECIMAL(4,2)
);

INSERT INTO ice_cream
(id, flavour, price)
VALUES
(1, 'Vanilla', 1.99),
(2, 'Chocolate Chip', 2.99),
(3, 'Raspberry Ripple', 3.99);

SELECT * FROM ice_cream --using SELECT at the ice_cream table

UPDATE ice_cream --using UPDATE to update the table
SET flavour = 'Mint Chocolate Chip' --using SET to set the flavour name
WHERE id = 2; --using WHERE to find the id of the icecream

DELETE FROM ice_cream --using DELETE to locate the ice_cream table
WHERE flavour = 'Raspberry Ripple' --WHERE to find which icecream to delete
--can also delete the icecream based on the id
--but id must be unique otherwise possibly deleting more icecream