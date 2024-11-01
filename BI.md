# Introduction to Business Intelligence
## Business Intelligence Topic
### Business Intelligence - Definition
Combines the following to help organisations make more data-driven decisions:  
1. Business Analytics  
2. Data Mining  
3. Data Visualization  
4. Data Tools  
5. Data Infrastructures  
6. Best practices
**Misconception:** Data generation is not a part of business analytics
### Business Intelligence - Evolution
Changed from "data sharing" to something that combines analytics, data mining, visualization, tools, infrastructures, and best practices to support "modelling for making decisions".
### Business Intelligence - Application
1. Preparing data for analysis
2. Developing and running queries
3. Creating reports, dashboards, and visualizations
### Business Intelligence - Goal 
Providing results to decision makers and end users
### Business Intelligence - Systems and Tools Components 
  1. Visuals
  2. Reports
  3. Apps
  4. Cards
  5. Databases
  6. Datasets
  7. Dataflows
  8. Filtering
  9. Drilling

## Analytical Hierarchy Topic
### Three primary types of analytics:
1. **Descriptive** - Describes what happened in the past. 
   e.g. report showing sales performance for last quarter
2. **Predictive** - Predicting what is likely to happen in the future.
   e.g. Sales revenue for next quarter is likely to increase by 5% compared to last quarter due to historical trend of increasing sales on average by 5% quarter on quarter.
3. **Prescriptive** - Suggests how we can make outcomes happen in the future.
   e.g. deploy new marketing promotion this month to ensure sales revenue next quarter increases by 5%.
### Two further types of analytics (extension):
4. **Diagnostic** - Helps explain why something happened in the past.
   e.g. sales increased last quarter due to higher lead to customer conversion last quarter because of more targeted marketing and lead engagement.
5. **Comparative** - comparing two different things in the same way. Typically combined with diagnostic analytics to find out similarities and differences (why the sales revenue differ).
   e.g. comparing sales revenue from two different states to find out which region performed better.
## Things to Know about Using AI and BI
1. **Humans are the key** - need right skills and expertise. e.g. developers and data scientists with experience
2. **Technology is not expensive** - open source/free developer tools for AI (and BI)e.g. CAFFE, TensorFlow, Microsoft Cognitive Toolkit, NLTK etc.
3. **AI (BI) is an application/tool not a solution to everything** - adding compute and knowledge to existing (good quality and relevant data) that makes it useful. 
4. **AI (BI) is not that smart** - Only as good as data ingested. Garbage in Garbage out concept applies here, collecting and structing data appropriately for AI (and BI) is imperative. Ai is more useful if proper data collection and transformations are applied to train models.
5. **AI (BI) is not for every problem** - Depends on needs and problem you are trying to solve. Discuss with an experts in industry and AI experts to decide if the problem can be solved with your current resources (data) and is suitable to solve using AI (BI). Lots of appropriate data for the problem is required and it should be used as a tool to aid in data-driven decision making process.
## Visualizations Topic
### Visualizations - Definition
A way to display data. e.g. Bar chart, waterfall chart, scatter plot
### Visualizations - Types
Graphs (Line), Tables, Maps (Heat, Tree, Choropleth), Charts (Bar, Waterfall, Ribbon, Gantt, Doughnut), Plots (Scatter), and Diagrams
### Visualizations - Selection and Design
Selecting and designing visualization depends on multitude of factors:
1. **Type of data**
2. **What we want to communicate**
3. **Level of data (drill up, drill down, drill through)**
4. **Aesthetic considerations e.g. colour**
E.g. Situation: Data analyst working for e-commerce company. Sales data for different product categories across multiple regions, goal is to create dashboard for senior management to review monthly performance.
1. **Type of Data available** - Numerical (Sales figures), Categorical (Product Categories) , Geographical (Regions), and Time Period (Monthly)
2. **What we want to communicate** - Objectives: Overall monthly sales trends, Sales performance comparison across different regions, Identify top-performing product categories, Provide option to drill down into specific regions/categories for detailed analysis
3. **Consider level of data** -  **Drill up:** Overview of total monthly sales, **Drill down:** detailed analysis by region/product category, **Drill through:** Further exploration to see individual transactions or customer demographics
4. **Aesthetic Considerations** - Use brand/product colours to differentiate product categories. Choose consistent colour palette for different regions. Ensure charts and graphs aren't overcrowded. Use labels and legends for clarity.
### Report vs Visualizations vs Dashboard
**Report:** Multi-perspective view into single dataset.
**Visualizations:** Represent different findings and insights from that dataset. Different view of data. Single visualization or many, a single page or many pages.
**Dashboard:** a single page, often called a canvas, <u>uses visualizations</u> to tell a story, consisting of multiple reports. Limited to one page, well-designed dashboard, contains only most important elements of story.
### Dataset, Dataflows, Data Drilling
**Dataset:** collection of data that you import or connect to.
- Imported data will always be snapshot in time
- Connected data updated as things change
**Dataflows:** processes that organize raw data into a format ready for visualization (and hence analytics).
- Set of queries that produce dataset ready for visualization
- Could be done in Database Management System
**Data Drilling:** Looking at different components of data in different ways - **interrogating data.**
- **Drilling up/Drilling down:** Explore next level down/up of detail. Done first in DBMS.
- **Drill through:** select part of visual and be taken to another page in report. Filtered to data that relates to part selected on original page.
- **Filter:** Removes data that doesn't apply. Conversely, <u>highlight greys</u> out data that doesn't apply.
# Introduction to Databases
## Database Topic
### Database - Definition
**Database** allows us to store, retrieve, change, and analyze data in a structured format. 
- It enables answering questions to make business decisions.
### Database - Key Concepts
 Databases are **organized collections** of data.
- Data is stored in a consistent and structured manner (e.g., tables, lists).
- **Tabular data** is the most common form, though databases differ from spreadsheets in functionality.
### Databases - Evolution (1960)
- Databases emerged in the 1960s, during a simpler computing era.
- Their development was **resource-limited**, mainly due to the lack of technological sophistication.
### Databases - First type of Database: Navigational Architecture
- The first databases used a **navigational architecture**.
- A **tree-like hierarchy** (parent-child relationships) was the main structure.
    - Parent could have multiple children (one-to-many).
    - This was useful but limited in flexibility to solve every data storage problem.
Here's the next section based on the content related to **Database Entities**:
### Database  - Component: Entities - Definition
**Entity** is something we store data about, represented by its **properties**.
Entities can be:
- **Tangible**: real-world objects (e.g., a person, location, machine).
- **Intangible**: conceptual things (e.g., system, product).
### Database  - Component: Properties - Definition
**Properties** define what makes an entity unique and how to describe it.
Examples:
- **Person** entity could have properties like `FullName`, `EmailAddress`, `BirthDate`.
- **Values** of these properties may differ between entities, but the properties themselves remain consistent.
### Databases -  Design : Relationships
#### 1. Parent-Child Relationship:
In databases, we focus on **entities** and their relationships rather than just data elements.
Common real-world relationships include **parent-child** structures.
- **Parent-child** relationships are not always present, but they are common.
- Example: An **Employee** can be a **Person** (parent-child relationship).
#### 2. Non-Parent-Child Relationships:
Some entities may not fit into a simple parent-child model, requiring other forms of relationship modeling
### Database - Design: Entity Relationship Diagrams (ERDs) - Definition
**Entity-Relationship Diagrams (ERDs)** visually represent the relationships between entities and their properties.
- They illustrate the elements of a database in terms of entities, properties, and relationships.
#### ERD - Key Points
ERDs help visualize how entities relate to one another.
- Various methods exist to create ERDs, and no single method is considered "the best."
- Different diagrams may show:
  - **Elements**: properties and entities.
  - **Relationships**: the way entities connect.
#### ERD - Example
- A simple ERD for a **Person** entity:
  - Properties: `FullName`, `EmailAddress`, `BirthDate`.
  - These properties connect to the **Person** entity, showcasing the relationship visually.
### Database - Structured Query Language (SQL)
 **SQL (Structured Query Language)** is used with **relational databases** to manipulate data.
#### SQL - Key Features
1. **Core Tasks**:
- **Create**: Defining new tables, databases, or other database objects.
- **View**: Querying and retrieving data.
- **Change**: Updating, deleting, or inserting new data.
- **Remove**: Deleting data or structures.
- **Administrative Tasks**: Managing users, defining models, and more.
1. **SQL as a Programming Language?**
- Some consider SQL a programming language, but it's more of a specialized language for database manipulation.
- **PL/SQL** and **extensions** add programming language-like functionality.
#### SQL - Modern Evolution
In some contexts, SQL has been replaced or complemented by **object-relational models**.
- These models allow databases to function similarly to **objects** in programming languages.
- This integration simplifies user-facing system development.
## Comparisons Topic
### Databases vs. Spreadsheets
#### Databases vs Spreadsheets - Key Differences
**Spreadsheets** are designed for simple data analysis and manipulation by a single user (or at least one user at a time).  
#### Databases vs Spreadsheets - Advantages of Databases
1. **Multiple Users**: Databases can support multiple people querying or interacting with the data at the same time.
2. **Performance**: Databases provide better performance for large data sets compared to spreadsheets.
3. **Access Control**: Databases offer finer-grained access controls for managing data security and user permissions.
### Data Model Formats
#### Traditional Relational Databases - Definition
**Relational databases** model data in tables composed of **rows** and **columns**.
#### Traditional Relational Databases -  Key Features
1. **Tables**: Data is stored in tables where each row is a record, and columns represent attributes of the data.
2. **Efficiency**: The format is efficient due to the regularity of structure—each row has the same columns.
3. **SQL and DBMS**: Manipulation of data within these models is typically done through **SQL** and a **database management system (DBMS)**.
#### Traditional Relational Databases - Alternative Models
- **NoSQL** databases (e.g., document databases) don't necessarily use rows and columns.
- Practical considerations include infinite rows and columns, but logical constraints exist.
Here's the Markdown note for the **Rows and Columns** section:
#### Relational Databases - Rows and Columns
In a **relational database**, one or more **tables** exist with **rows** and **columns**.
##### Relational Databases - Rows and Columns - Key Features
1. **Rows**:
   - Represent **observations** or **records**.
   - Each row identifies a unique occurrence of an activity, phenomenon, or entity.
2. **Columns**:
   - Represent **attributes** of the table.
   - Define what is being measured or described in each record.
##### Relational Databases -  Additional Concepts: Normalization
**Normalization**: Ensures that the attributes in each table are logically related to minimize the duplication of data.
- Tables can contain both related and seemingly unrelated attributes, but normalization reduces redundancy.
#### Other Database Structures
**Relational databases** are common but not the only type. Depending on the situation, other models may be more suitable.
##### Other Database Structures - Types of Database Structures
1. **Object-Oriented Databases**:
- Models **objects** (instances, i.e., rows) of entities or things (e.g., products, employees).
- Attributes or properties are similar to **columns** in relational databases.
2. **Distributed Databases**:
- Data is stored across multiple locations or machines.
- Pros: Can provide fault tolerance and scalability.
- Cons: Complexity in managing and querying distributed data.
3. **Data Warehouses**:
- A **centralized repository** for quick retrieval of data for analysis.
- The opposite of distributed databases, optimized for read-heavy operations.
4. **NoSQL Databases**:
- "Not only SQL" or **non-relational** databases.
- Stores less structured (unstructured or semi-structured) data.
- Example: **MongoDB**, often used in web applications.
- Pros: Flexibility with unstructured data.
- Cons: Can lack the consistency of traditional relational databases.
5. **Graph Databases**:
- Stores data as **nodes** (entities) and **edges** (relationships between nodes).
- Ideal for complex relationships (e.g., social networks).
6. **OLTP Databases**:
- **Online Transactional Processing** systems designed for performance and simultaneous operations.
- Handles high volumes of small, simple transactions.
7. **Open-source Databases**:
- Example: **MySQL**.
- Source code is available for modification and reuse.
8. **Cloud Databases**:
- Databases stored in the cloud, offering distributed access and simplified management.
9. **Multimodel Database**:
- Combines multiple data models, providing flexibility and benefits of each.
10. **Document (JSON) Database**:
- Stores data as **JSON** documents (key-value pairs) rather than in relational tables.
## Database Software Topic
#### Database Software - Overview
Many software tools exist for manipulating databases, either through graphical interfaces or text-based interfaces.
Example: **MySQL Workbench** – a graphical interface.
Common tasks include:
  1. Data retrieval and manipulation.
  2. Model definition and modification.
  3. Backup, reporting, and user access management.
  4. Security controls.
#### Database Software - Graphical vs. Text-Based Interfaces
Both interface types offer benefits, and neither is inherently better.
- **Graphical interfaces** simplify tasks and help ensure they are completed correctly.
- Important in terms of **data integrity** and **security**.
#### Software - Database Management Systems (DBMS)
 **DBMS** is an interface between the database and the user, allowing interactions and commands.
  - Used for:
    1. Data manipulation.
    2. Administrative tasks.
- Often, **end user** is not physical but may be a **machine** running software to interact with the system.
- **DBMS** and database are often considered inseparable – database can't function without the DBMS.
#### Software -  MySQL Databases
 **MySQL** is a popular relational DBMS because:
  - Works across many platforms (client and server).
  - Free to download and use, flexible, and powerful.
  - Used by popular web applications like Airbnb, LinkedIn, YouTube, and Twitter.
**Other examples of relational DBMS include:**
  1. Oracle
  2. PostgreSQL
  3. MSSQL (Microsoft SQL)
  4. MariaDB
  5. Amazon databases
#### Software - Business Decision Making & Databases
Databases are vital to **Business Intelligence (BI)**, helping businesses make decisions by storing, processing, and analyzing vast amounts of data.
- Sensor systems (e.g., IoT) generate large amounts of data that databases help analyze to pick up patterns and insights.
- **BI tools** linked to databases provide businesses with the capability to:
  1. Make quicker decisions.
  2. Achieve better business efficiency.
  3. React faster to changes (agility) and grow (scale) quicker.
#### Software - Self-Driving Databases
**Self-driving databases** use **AI/ML** to automate management tasks, making them somewhat autonomous.
  - These databases can **secure** and **repair** themselves automatically, lowering the need for database administrators.
  - This reduces costs, improves security, and enhances performance.
#### Software - Database Challenges
**Challenges in database management** include:
1. Handling large increases in data volume (e.g., IoT, sensors).
2. Ensuring **data integrity** and organization.
3. **Security** of personal/private data to meet legal requirements and prevent breaches.
4. Managing end-user demand for timely data access.
5. Protecting databases from threats and patching systems.
6. Planning for **scalability** in advance, especially with performance and data sovereignty issues.
# Database Keys and Design Topic
## Database Keys - Definition
**Keys** are used in relational databases as an attribute to uniquely identify individual rows.
- **Primary Key (PK)**: A unique identifier for each record within a table.
- **Foreign Key (FK)**: A reference to a PK in another table to establish relationships between tables.
- Relationship allows the second table to extend the values and attributes defined within the first table.
#### Database  Keys - Characteristics
**Keys** are automatically increasing numeric values but can be of other types (text-based or integer-numeric formats).
Performance of these keys should be considered when using unusual formats, as they are essential for efficient lookups.
- Example: Using images as primary keys would be inefficient.
- **Indexes**: Built for searching keys, enhancing performance.
#### Database Keys - Relationships
**Relationship** created when a foreign key in one table matches a primary key in another table.
**Cardinality** describes the type of relationship:
- **One to Many (1:M)**: One record links to many records in another table.
- **Many to One (M:1)**: Many records link to one record in another table.
- **One to One (1:1)**: One record links to exactly one record in another table.
#### Database Keys - Relationship Types : Many to Many
**Many to Many (M:M)**: Complex relationship where many rows in one table link to many rows in another table.
- Typically requires a linking table with primary keys from both tables.
- Graph databases may be better suited for **M:M** use cases.
#### Database Keys - Entity-Relationship (ER) Diagrams
ER diagrams visually represent relationships between entities, with labels for cardinality.
- Example: A "Person" entity may be linked to an "Organisation" entity through the relationship "Employed By," showing cardinality (1 to N).
### Database Keys - Designing a Database
#### Database Keys - Database Design Tasks
- **Define entities**: Identify the sets of entities for the system.
- **Determine tables**: Decide what tables are needed based on the entities.
- **Identify keys**: Define the primary and foreign keys for each table.
- **Describe cardinality**: Specify the relationships between entities.
- **Identify attributes**: Define and list the attributes for each entity.
#### Database Keys - Importance of Design
Poor design leads to inefficient databases.
- The exercise of creating a database should align with needs and avoid future complications.
- **Practice**: Continuously practicing database design helps refine the approach and identify potential problems early.
#### Database Keys - Design Without DBMS
Designing databases manually (without a DBMS) helps in understanding the structure, but it may not always be the best or only way.
SQL Basics
# SQL Basics
## SQL - Building a Database
### SQL - Building a Database: Steps
1. Define entities and their relationships.
2. Determine required attributes (fields) for each entity.
3. Identify Primary and Foreign keys.
4. Populate database with data after setting up and building the model.
### SQL - CRUD Operations
- **CRUD:** Create, Read, Update, Delete – the four main operations in any storage system:
- **Create**: Add new data to the system (including data modelling).
- **Read**: Retrieve data or model that exists.
- **Update**: Modify existing data or model.
- **Delete**: Remove a record from the system.
### SQL - ACID Principles
- **ACID:** Ensures data validity in databases:
- **Atomicity**: Treat each command as a whole or not at all.
- **Consistency**: Ensure data in database remains valid.
- **Isolation**: Ensure concurrency does not affect the outcome. Concurrent transactions result in the same output as sequential execution.
- **Durability**: Ensure changes are permanent after they are made, even after system failure.
### SQL - Building a Database: Creating a Database
- **Building Block**: In MySQL, a database is the core structure.
- Databases contain **tables**, which in turn store rows and columns.
- Before creating tables, a database must be created to hold the data.
### SQL - Creating a Table
- **Structure**: Tables contain columns (attributes) and rows (records).
- **Prefix tables with the database name**, e.g., `<StudentID>_db.<TableName>`.
- Define each column with its **data type** and any special **modifiers**.
### SQL - Table and Database Relationships
- **Hierarchy and Structure**:
  - DBMS > Databases > Tables > Columns/Rows.
  - **Permissions**: Access rights can vary across tables and databases.
#### SQL - Creating a Table: CREATE TABLE
**CREATE TABLE** command:
```sql
CREATE TABLE <DatabaseName>.<TableName> (
    <ColumnName> <DataType> <Modifiers>,
    PRIMARY KEY (<ColumnName>)
);
```
**CREATE TABLE** example:
```sql
CREATE TABLE 12345678_db.TestTable (
    id int NOT NULL,
    name varchar(255),
    creationDate date,
    PRIMARY KEY (id)
);
```
#### SQL - MySQL Data Types
- **DATE:** Stores dates in `YYYY-MM-DD`.
- **TIME:** Stores times in `HH:MM:SS`.
- **DATETIME:** Stores both date and time.
- **VARCHAR(X):** Variable length string.
- **CHAR(X):** Fixed length string.
- **BOOLEAN:** TRUE/FALSE stored as 0 or 1.
- **INT:** Integer (whole number).
- **FLOAT:** Floating point number.
#### SQL - Other Data Types
- Other data types include **JSON documents**, **binary strings**, and **blobs** (for storing images or spatial data).
- Numeric formats like **TINYINT** handle specialized cases.
### SQL - Attribute (Field) Modifiers
- **PRIMARY KEY:** Designates a column as unique identifier.
- **AUTO_INCREMENT:** Automatically increases integer value for each row.
- **NOT NULL:** Ensures no missing values in that column.
- **FOREIGN KEY:** Establishes relationships between tables.
#### SQL - Modifying a Table: ALTER TABLE
**ALTER TABLE** commands modify the table structure without recreating it.
**ALTER TABLE** Adding a column:
```sql
ALTER TABLE <TableName> ADD COLUMN <ColumnName> <DataType> <Modifiers>;
```
**ALTER TABLE** Removing a column:
```sql
ALTER TABLE <TableName> DROP COLUMN <ColumnName>;
```
#### SQL - Altering a Field: ALTER TABLE
**Change or Rename a column**:
**Renaming Field:**
```sql
ALTER TABLE <TableName> RENAME COLUMN <OldColumnName> TO <NewColumnName>;
```
**Modifying Field:**
```sql
ALTER TABLE <TableName> MODIFY COLUMN <ColumnName> <DataType> <Modifiers>;
```
#### SQL - Deleting a Table
**DROP TABLE** command deletes a table and all its data:
```sql
DROP TABLE <TableName>;
```
### SQL - Scripts in MySQL
#### SQL - Running a 'script' in MySQL
**Shortcut to help save time during analysis.**
  - Useful when issuing many commands to effect something.
  - Helps ensure that commands are entered correctly before issuing.
  **Solution:**
  - Use the **script function** of MySQL Workbench.
  - Allows running a file full of SQL commands we have authored.
  - These commands are executed immediately, one after another, from top to bottom.
#### SQL - MySQL: Steps to running a 'script'
**Definition:** Whether it's considered a script or not depends on context (like a set of commands executed automatically).
  **Steps:**
1. Write the commands using MySQL Workbench, one by one, and save the file with a `.sql` extension.
 - Built-in functions can help save these commands.
 - **Important:** One command per line, ending with a semicolon.
- **Execution:**
  - Once a command is run, it is updated instantly on the database server.
  - You may use `#` to comment out lines that have already run.
### SQL - Generated Columns
**Generated column** is an attribute/column not directly set for each observation. Its value is calculated from a mathematical function on other columns.
- If columns it depends on are set (and not null), the value for this column is set automatically.
- Helpful for summarizing and analyzing data on the fly.
#### SQL - Create Generated Columns Command
The main phrase used to create a generated column is:  
 **GENERATED ALWAYS AS (`function`)**
- Where `<function>` involves one or more other columns.
- Specify either **VIRTUAL** or **STORED** before the semicolon to decide when the calculation occurs.
- **VIRTUAL**: Result calculated dynamically every time column is accessed. For frequently changing data where calculated values are rarely accessed, minimising storage, real-time calculations needed for latest data.
- **STORED**: Result calculated once and saved in table. For rarely changing data where calculated values are frequently accessed, indexing on calculated column is necessary.
##### Example of Generating a Column:
```sql
CREATE TABLE Example(
  id INT NOT NULL AUTO_INCREMENT,
  isTrue BOOLEAN,
  someQuantity INT,
  otherQuantity INT,
  combinedQuantity INT GENERATED ALWAYS AS (someQuantity * otherQuantity) <TYPE OF GENERATED COLUMN>,
  PRIMARY KEY (id)
);
```
- Creates a table where `combinedQuantity` is automatically generated as the product of `someQuantity` and `otherQuantity`, by default `VIRTUAL`.

### Types of Generated Columns
#### Functions with Generated Columns:
**CONCAT()**: Used to concatenate multiple text fields.
**Arithmetic functions**: Can be applied on numeric columns (e.g., `+`, `-`, `*`, `/`).
##### Example:
```sql
CREATE TABLE Example(
  id INT NOT NULL AUTO_INCREMENT,
  someText1 VARCHAR(255),
  someText2 VARCHAR(255),
  fullText VARCHAR(255) GENERATED ALWAYS AS (CONCAT(someText1, someText2)),
  PRIMARY KEY (id)
);
```
- This table automatically concatenates `someText1` and `someText2` to form `fullText`.
- Generated columns are automatically updated when the columns they depend on are modified.
- Generated columns help avoid storing redundant data by calculating values as needed.
### SQL - Modifiers and Constraints
#### Constraints - Definition
- **Definition**: Constraints are rules enforced on columns to maintain **data integrity** and **accuracy** in a table.
- **Types of Constraints**:
- **Primary Key**: Ensures each row in a column is unique and not NULL.
- **Foreign Key**: Links a column to another table’s primary key to enforce referential integrity.
- **Unique**: Ensures all values in a column are unique.
- **Not Null**: Ensures that a column cannot contain NULL values.
- **Default**: Sets a default value for a column when no value is provided.
- **Check**: Sets a condition that values in a column must meet (e.g., `CHECK (age > 18)`).
#### Modifiers
- **Definition**: Modifiers are SQL commands used to alter the structure or properties of a table’s columns, including adding, removing, or updating constraints.
- **Examples of Modifiers**:
- **ALTER TABLE**: Used to modify the structure of a table.
- **DROP**: Used to remove an existing constraint (e.g., `DROP PRIMARY KEY`).
- **ADD**: Adds a new constraint to a column (e.g., `ADD PRIMARY KEY`).
- **MODIFY**: Changes column properties (e.g., setting a column to `NOT NULL` or adding a `DEFAULT` value).
#### Modifiers - Removing and Recreating Primary Key
**Primary key** cannot be modified with a regular `MODIFY` command.
- Must be removed using `DROP PRIMARY KEY` command:
  ```sql
  ALTER TABLE <TableName> DROP PRIMARY KEY;
  ```
- After removing, can re-create the primary key:
  ```sql
  ALTER TABLE <TableName> ADD PRIMARY KEY(<ColumnName>);
  ```
#### Additional Modifiers / Constraints
- **DEFAULT**: Sets a default value for a column.
  ```sql
  DEFAULT <defaultValue>;
  ```
- **CHECK**: Adds a condition that must be satisfied for a value to be added or changed in a column.
  ```sql
  CHECK (<formula>);
  ```
- Constraints can be named for clarity:
  ```sql
  CONSTRAINT <name> CHECK (<formula>);
  ```
#### Example Modifiers
- **Set default for a BOOLEAN**:
  ```sql
  ALTER TABLE Example MODIFY COLUMN isTrue BOOLEAN DEFAULT 1;
  ```
- **Make column NOT NULL**:
  ```sql
  ALTER TABLE Example MODIFY COLUMN someQuantity INT NOT NULL;
  ```
- **Add a CHECK constraint**:
  ```sql
  ALTER TABLE Example ADD CONSTRAINT sqCons CHECK (someQuantity > 0);
  ```
#### Constraints on Tables
- Apply constraint to existing attribute:
  ```sql
  ALTER TABLE <TableName> ADD CHECK (<formula>);
  ```
- Or using `CONSTRAINT` format:
  ```sql
  ALTER TABLE <TableName> ADD CONSTRAINT <name> CHECK (<formula>);
  ```
- Remove a constraint:
  ```sql
  ALTER TABLE <TableName> DROP <constraint>;
  ```
- Can replace `ADD` with `DROP` to remove constraints.
### SQL - WHERE Clauses
#### WHERE Clause - Concept
- Used with normally with **SELECT**, applies a command only to a subset of rows/observations.
- Example: `id = 1` (matches a column to a single value).
##### WHERE Clause Limitation
- Only matching a column to a single value is limited.
- For more complex formulas, we use operators and keywords.
#### WHERE Operators
- **=**: Equal (the same) - does not work for floating point values.
- **>**: Greater than (numeric types).
- **<**: Less than.
- **>=**: Greater than or equal to.
- **<=**: Less than or equal to.
- **<>**: Not equal to (sometimes written as `!=`).
- **BETWEEN**: Matches values within a range (`x AND y`).
- **LIKE**: Basic pattern matching (`%` as wildcard).
- **IN**: Matches a value from a comma-separated list.
#### WHERE Keywords
- **AND**: Both sides must be true to match.
- **OR**: Either side must be true to match.
- **NOT**: Applies to one formula, gets the opposite result.
- **NOT** can be combined with **AND** or **OR**.
- Use brackets for clarity when combining.
#### Example of Complex WHERE Clause
```sql
SELECT (date, customerName)
WHERE (transactionItem > 2) AND (date BETWEEN '2023-01-01' AND '2023-12-31');
```
### SQL - Foreign Keys
#### Foreign Keys Definition
**Foreign keys** establish a link between tables.
- The 'other' table and its primary key must exist before a foreign key relationship can be created.
- Defined similarly to primary keys but references another table's column.
#### Foreign Key Syntax
- **Syntax**: `FOREIGN KEY (<AttributeName>) REFERENCES <TableName>(<ColumnName>)`.
- Can be named as a constraint: `CONSTRAINT <ConstraintName> FOREIGN KEY <AttributeName> REFERENCES <TableName>(<ColumnName>)`.
#### Foreign Key Requirements
- **Foreign key** must be defined as an attribute in the current table.
- Example: If `OrderID` is a foreign key, it should be defined in the table as an `int` attribute.
#### Foreign Keys - Modify
- **Add foreign key**: `ALTER TABLE <TableName> ADD FOREIGN KEY...`.
- **Add constraint:** `ALTER TABLE <TableName> ADD CONSTRAINT...`.
- **Drop foreign key:** `ALTER TABLE <TableName> DROP FOREIGN KEY...`.
#### Foreign Keys - Constraints
**Constraints** define actions when the referenced row is deleted or updated.
- Syntax: `ON DELETE <method>`, `ON UPDATE <method>`.
#### Foreign Keys - Constraint Referential Actions
- **CASCADE**: Delete or update the referring rows when the referenced row is deleted/updated.
- **SET NULL**: Set referring attribute to NULL when the referenced row is deleted.
- **RESTRICT**: Prohibit the delete or update action if referenced elsewhere.
- **NO ACTION**: Same as RESTRICT, but more explicit.
#### Foreign Key Constraints Example
```sql
CREATE TABLE Invoice (
id INT AUTO_INCREMENT,
customerID INT,
FOREIGN KEY (customerID) REFERENCES Customer(id) ON DELETE CASCADE
);
```
### SQL - Indexes
**Indexes** speed up data retrieval on primary keys or other attributes.
  - Uses processing power and storage but is invisible to users.
  - Indexed attributes are quicker to query.
- **Create an index** with:
  - `CREATE UNIQUE INDEX <IndexName> ON <TableName>(<AttributeName>);`
  - `CREATE INDEX <IndexName> ON <TableName>(<AttributeName>);`
  - `CREATE INDEX <IndexName> ON <TableName>(<AttrOne>, <AttrTwo>);`
- `<IndexName>` is the name for the index, `<TableName>` is the table name, `<AttrOne>`, `<AttrTwo>` are attribute names.
- **Remove an index**:
  - `DROP INDEX <IndexName>;`
  - Drops only the index, not the table or its data.
- **Additional index options**:
  - Can specify how the index is created (e.g., if it’s **modifiable - default**  or fixed).
### SQL -  Tips
#### SQL -  `USE` Command
- Issue `USE` command once per session to select a database.
- Reissue `USE` if reconnecting to database server.
- Issue different `USE` command to switch databases; no cancellation needed.
- Issuing `USE` for the same database again has no effect.
- Include `USE` as the first line in SQL scripts.
- **Example**: 
	```sql
	USE my_database; SELECT * FROM customers;
	 ```
#### SQL - Commenting Queries
- Comments provide explanations for future reference.
- Useful for understanding complex queries.
- Can assist others reviewing the query.
- **Three types of comments:**
	- `#` for line comments. 
	- Example: `# Select all records` 
	- `--` for line comments. 
		- Example: `-- Fetch all customer names` - `/* ... */` for block comments over multiple lines. 
	- `/* ... */` for block comments over multiple lines.
	- Example: 
	```sql
		/* This query calculates total sales for each customer */ 
		SELECT customer_id, SUM(sales) FROM orders GROUP BY customer_id;
	```
- Comments are ignored during execution.
#### SQL - `SHOW CREATE TABLE` Command
- `CREATE TABLE` command defines the data model.
- `ALTER TABLE` command modifies the table structure.
	- Example: `ALTER TABLE students ADD COLUMN grade CHAR(1);`
- `SHOW COLUMNS FROM <TableName>` displays column info but excludes constraints.
	- Example: `SHOW COLUMNS FROM students;`
- `SHOW CREATE TABLE <TableName>` shows the full table definition, including constraints.
	- Example: `SHOW CREATE TABLE students;`
- **Practical Example**:
```sql
CREATE TABLE `TransactionItem` (
`id` int NOT NULL AUTO_INCREMENT,
`description` varchar(255) NOT NULL,
`quantity` int DEFAULT NULL,
`unitPrice` float DEFAULT NULL,
`hasGst` tinyint(1) DEFAULT '0',
`totalPrice` float GENERATED ALWAYS AS ((`unitPrice` * `quantity`)) STORED,
`taxAmount` float GENERATED ALWAYS AS ((`hasGst` * (`unitPrice` / 11))) STORED,
PRIMARY KEY (`id`),
UNIQUE KEY `TransactionItemIndex` (`id`),
CONSTRAINT `qConstraint` CHECK ((`quantity` > 0)),
CONSTRAINT `upConstraint` CHECK ((`unitPrice` > 0))
) ENGINE=InnoDB AUTO_INCREMENT=5 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
```
#### SQL - Adding Multiple Values at Once
- Syntax: `INSERT INTO <TableName> (<Columns>) VALUES (<Values>)`.
- Use commas to separate multiple sets of values.
	- Example: 
```sql
	INSERT INTO students (id, name, age) VALUES (1, 'Alice', 20), (2, 'Bob',       22);
```
- No need to specify columns if all are included in `<Values>`.
	- Example: 
	```sql
	INSERT INTO students VALUES (3, 'Charlie', 23), (4, 'Daisy', 24);
	```
- **Advantage**: less code for multiple entries.
- **Disadvantage**: harder to debug errors.
#### SQL - Special Columns
- Use `DEFAULT` for auto-incrementing and generated columns.
- Example: `INSERT INTO <TableName> VALUES (DEFAULT, "Test", ...)`.
```sql
	INSERT INTO students (id, name, age) VALUES (DEFAULT, "Test", 21);
```
### SQL - Sorting Data
**Purpose of Sorting**: to identify largest, smallest, or average values. Find most or least common values.
- Example: Sort prices in descending order to see the highest price first.
**Types of Sorting**: Numeric and date types: sort smallest to largest (ascending) or largest to smallest (descending).
- Example: Sort order amount in ascending order.
- Text types: sort alphabetically A to Z or Z to A.
- Example: Sort customer names alphabetically.
**Multi-column Sorting**: Sort by multiple columns: primary column first, then secondary if values in the primary column are equal.
- Example: Sort by `last_name`, then by `first_name` if last names are the same.
**SQL Syntax for Sorting**: Use `ORDER BY` clause at the end of `SELECT` query.
  - List columns to sort by, separated by commas.
  - Specify `ASC` for ascending (default) or `DESC` for descending.
    - Example: `SELECT * FROM Customers ORDER BY last_name ASC, first_name DESC;`
- **Practical Example**  
  - `SELECT customerName FROM Transaction ORDER BY transactionItem ASC;`
    - Sorts customer names based on `transactionItem` in ascending order.
    - Result: List of customer names ordered by `transactionItem` values.
### SQL - Grouping and Aggregation
 **Purpose**: Aggregates data based on shared values to understand properties of rows in groups.
  - Example: Group items without GST in `TransactionItem` to view their properties.
- **Grouping Columns**: Identify which columns to group by to get meaningful groups.
  - Example: `GROUP BY hasGst` groups items based on whether they have GST.
- **Filter Before Grouping**: Use `WHERE` to filter rows before grouping to narrow down results.
#### SQL - GROUP BY Clause
- **Position**: Sits between `WHERE` and `ORDER BY` clauses.
- **Columns**: Specify columns to form the grouping in order of priority.
- Example: `GROUP BY hasGst, date` groups by GST status, then by date.
#### SQL - Aggregating Functions
- **Purpose**: Specify how values in each group are summarized.
- **Common Functions**:
  - `AVG(column)`: Mean of values.
    - Example: `AVG(price)` to find average price in each group.
  - `MIN(column)`: Smallest value.
    - Example: `MIN(price)` for lowest price in each group.
  - `MAX(column)`: Largest value.
    - Example: `MAX(price)` for highest price in each group.
  - `SUM(column)`: Total of values.
    - Example: `SUM(quantity)` for total quantity in each group.
  - `COUNT(column)`: Count of values.
    - Example: `COUNT(id)` for the number of items in each group.
#### SQL -  Date Functions in GROUP BY
 **Functions**:
  - `MONTH(column)`: Group by month.
    - Example: `GROUP BY MONTH(date)` groups by month.
  - `YEAR(column)`: Group by year.
    - Example: `GROUP BY YEAR(date)` groups by year.
  - `NOW()`: Current date/time, often used in `WHERE`.
#### SQL - Example Query
```sql
SELECT hasGst, MAX(unitPrice)
FROM TransactionItem
GROUP BY hasGst;
```
 **Interpretation**:
  - For `hasGst = 1`, max `unitPrice` is 123.45.
  - For `hasGst = 0`, max `unitPrice` is 100.
#### SQL - Aggregation and Grouping Example
```sql
SELECT department, MONTH(date), YEAR(date), COUNT(id), MIN(salePrice)
FROM ExampleTable
WHERE department LIKE 'SALES %'
GROUP BY department, MONTH(date), YEAR(date)
ORDER BY MIN(salePrice) DESC;
```
 Groups by department and month/year, counts items, finds minimum sale price, and sorts results.
#### SQL - Alias
**AS Alias**: Simplifies column names in output.
- Example: `MIN(price) AS minPrice`.
- **WITH ROLLUP**: Adds grand totals in grouped results.
- **NULL Handling**: Aggregation functions ignore `NULL` values by default.
**Example**:
```sql
SELECT department AS Dept,         -- Alias for department column
MONTH(sale_date) AS SaleMonth,     -- Alias for month extracted from sale_date
YEAR(sale_date) AS SaleYear,   -- Alias for year extracted from sale_date
COUNT(id) AS SaleCount,        -- Alias for counting sales entries
MIN(sale_price) AS MinSalePrice -- Alias for minimum sale price
FROM SalesData
GROUP BY department, YEAR(sale_date), MONTH(sale_date)
WITH ROLLUP           -- Adds subtotals and grand totals for the grouped columns
ORDER BY 
department, SaleYear, SaleMonth;
```
- An additional cell row of all null values and MinSalePrice will have total due to WITH ROLLUP
### SQL - Joining Tables
#### Joining Tables Introduction
- **Foreign Key**: Used to refer to a row in one table from another, creating a reference.
- **Row Extension**: Joining tables extends rows by combining data from both tables.
####  Joining Tables Logic
- **JOIN Query**: Combines two tables using a specific condition to match rows.
- **Matching Columns**: The condition specifies which columns in each table should match.
- **Relationships**: Can handle various types (e.g., one-to-many, many-to-many).
#### Types of Joins
- **LEFT JOIN**: Keeps all rows from the first (left) table, matching rows from the second (right) table.
- **RIGHT JOIN**: Keeps all rows from the second (right) table, matching rows from the first (left) table.
- **INNER JOIN**: Only keeps rows that match in both tables.
- **Choosing Join Type**: Depends on the context and the desired data outcome.
- **UNIONS**: Can be used to combine results of different joins to see all observations.
#### Visual Representation of Joins
- **LEFT JOIN**: Shows all data from the left table, matching with the right.
- **INNER JOIN**: Shows only overlapping data from both tables.
- **RIGHT JOIN**: Shows all data from the right table, matching with the left.
#### Syntax Format of Joins
- **Basic JOIN Syntax**:
  ```sql
  SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
  ```
- **ON Clause**: Specifies which columns to match in each table.
- **Using Aliases**: Can use `AS` to simplify or differentiate column names.
#### Joins in Practice
- **Example**:
  - **TableOne**:
    | idOne | dataOne     |
    |-------|-------------|
    | 1     | Hello       |
    | 2     | What's      |
    | 3     | Happening   |
  - **TableTwo**:
    | idTwo | dataTwo     |
    |-------|-------------|
    | 2     | World       |
    | 4     | Up          |
    | 6     | Now!        |
  - **INNER JOIN Example**:
	```sql
	SELECT * FROM TableOne INNER JOIN TableTwo ON TableOne.idOne =                 TableTwo.idTwo;
	```
	Result:
    | idOne | dataOne | idTwo | dataTwo |
    |-------|---------|-------|---------|
    | 2     | What's  | 2     | World   |
  - **LEFT JOIN Example**:
    ```sql
    SELECT * FROM TableOne LEFT JOIN TableTwo ON TableOne.idOne =                  TableTwo.idTwo;
    ```
    Result:
    | idOne | dataOne     | idTwo | dataTwo |
    |-------|-------------|-------|---------|
    | 1     | Hello       | NULL  | NULL    |
    | 2     | What's      | 2     | World   |
    | 3     | Happening   | NULL  | NULL    |
  - **RIGHT JOIN Example**:
    ```sql
    SELECT * FROM TableOne RIGHT JOIN TableTwo ON TableOne.idOne =                 TableTwo.idTwo;
    ```
    Result:
    | idOne | dataOne     | idTwo | dataTwo |
    |-------|-------------|-------|---------|
    | 2     | What's      | 2     | World   |
    | NULL  | NULL        | 4     | Up      |
    | NULL  | NULL        | 6     | Now!    |
  - **FULL OUTER JOIN Example** (Using `UNION` of LEFT and RIGHT JOIN results):
    ```sql
    SELECT * FROM TableOne LEFT JOIN TableTwo ON TableOne.idOne = TableTwo.idTwo
    UNION
    SELECT * FROM TableOne RIGHT JOIN TableTwo ON TableOne.idOne = TableTwo.idTwo;
    ```
    Result:
    | idOne | dataOne     | idTwo | dataTwo |
    |-------|-------------|-------|---------|
    | 1     | Hello       | NULL  | NULL    |
    | 2     | What's      | 2     | World   |
    | 3     | Happening   | NULL  | NULL    |
    | NULL  | NULL        | 4     | Up      |
    | NULL  | NULL        | 6     | Now!    |
### SQL - Views on Tables
**Purpose of Views**: Generate a new table from the result of a `SELECT` query.
  - Can be a filtered version of a single table (e.g., using `WHERE`).
  - Can be the result of a `JOIN` between two tables.
- **Accessing Views**: Access the view like any other table.
  ```sql
  SELECT * FROM ViewName;
  ```
#### Syntax of Creating a View
- **Creating a View**:
  ```sql
  CREATE VIEW <ViewName> AS SELECT ...
  ```
- **Updating a View**:
  ```sql
  CREATE OR REPLACE VIEW <ViewName> AS SELECT ...
  ```
- **Deleting a View**:
  ```sql
  DROP VIEW <ViewName>;
  ```
- **Show View Definition**:
  ```sql
  SHOW CREATE VIEW <ViewName>;
  ```
#### Examples of Views
- **Basic View**:
  ```sql
  CREATE VIEW ExampleView AS SELECT * FROM ExampleTable;
  ```
- **Filtered Column View**:
  ```sql
  CREATE VIEW ExampleViewTwo AS SELECT AttributeOne FROM ExampleTable;
  ```
- **Aggregated View**:
  ```sql
  CREATE VIEW ExampleViewThree AS 
  SELECT AttributeThree, MAX(AttributeTwo) 
  FROM ExampleTable 
  WHERE AttributeThree < 9000 
  GROUP BY AttributeThree 
  ORDER BY AttributeThree DESC;
  ```
#### SQL - Spatial Databases
- **Spatial Data**  
  - Describes physical location of each observation in the real world.
  - Uses latitude and longitude to specify locations.
- **Spatial Reference System**  
  - Specifies how a location is described, typically using latitude and longitude.
- **Types of Spatial Data**  
  - Commonly includes points, lines, and polygons.
  - In this context, we focus on point data.
- **Longitude and Latitude**  
  - **Longitude**: Runs along the east-west direction.
  - **Latitude**: Runs along the north-south direction.
- **Creating Point Data in MySQL**  
  - Define a spatial attribute using `geometry POINT`.
    ```sql
    CREATE TABLE GeometryTable (geometry POINT);
    ```
  - Insert spatial data with specific format:
    ```sql
    INSERT INTO GeometryTable VALUES (ST_GeomFromText('POINT(Long Lat)'));
    ```
    - Example: `POINT(114.5 -23.7)` for specific longitude and latitude.
- **Spatial Queries**  
  - Filter data within a certain distance from a point using `ST_Distance_Sphere`.
    ```sql
    SELECT * FROM <TableName> 
    WHERE ST_Distance_Sphere(<GeomField>, ST_GeomFromText(<Location>)) <= 10 * 1000;
    ```
  - Useful for finding locations within a specific radius.
- **Viewing Geometries as Text**  
  - Use `ST_AsText` to view geometry data in readable format.
    ```sql
    SELECT ST_AsText(<FieldName>) FROM <TableName>;
    ```
  - Helps when visualizing geometry fields without cryptic characters.
### SQL - Loading Spreadsheets
**Purpose**: Translate spreadsheet data into a database to leverage database advantages over spreadsheets.
**Challenges**: Crafting `INSERT` queries for each row is time-consuming.
#### Automating `INSERT` Queries
**Automated Solution**: Generate `INSERT` queries based on spreadsheet content.
- Example tool: [TableConvert](https://tableconvert.com/excel-to-sql) for converting Excel to SQL.
#### Alternate Loading Method with `LOAD DATA`
- **Command**: Use `LOAD DATA INFILE '<FileName>' INTO TABLE <TableName>;`
  - Requires full file path or correct folder location.
  - **Pre-requisite**: Must `CREATE TABLE` with schema matching file format before loading.
#### Modifiers for Loading Data
- **IGNORE `<X>` LINES**: Skips the first `<X>` lines of the file.
- **Column List**: Load specific columns by listing them in the `INSERT` statement.
- **SET `<ColumnName> = <Value>`**: Set specific columns to a fixed value.
- **`@var<X>`**: Reference column `<X>` in the input file for conditional data manipulation.
## Power BI - Basics
**Power BI**: Suite of business intelligence tools by Microsoft.
  - **Power BI Desktop**: Windows application for building dashboards and reports. Not available on macOS.
  - **Power BI Online**: Web-based version with limited features for creating and sharing dashboards.
  - **File format**: Power BI Desktop files have a `.pbix` extension.
#### Interface Overview
- **Power BI Desktop Interface Components**:

  ![Pasted image 20241026140547.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/13d319fc9371f70a442bde8669113f0822ff823f.png "wikilink")

  - **(1)** Pages Panel: Shows the different pages of the report.
  - **(2)** Fields Pane: Lists the available data fields.
  - **(3)** Visualizations Pane: Contains visualization types.
  - **(4)** Filters Pane: Filters for the visualizations and reports.
  - **(5)** Ribbon: Contains various tools and options for managing data, visuals, and settings.
  - **(6)** Sidebar: Navigation for different views (Report, Data, Model).
  - **(7)** Page Tabs: Tabs for different pages within the report.
  - **(8)** Data Source Options: Options to import data from Excel, SQL Server, etc.
#### PowerBI - Creating a Report
- Steps to create a basic report:
  - Import data (e.g., Excel workbook).
  - Create visuals and charts using fields from the data pane.
  - Organize visuals on a report page.
#### PowerBI - Data Transformation
- **Transform Data**: Prepares data by modifying its format for analysis.
  - **Operations**:
    - Derive new attributes.
    - Adjust data shape (rows/columns).
    - Change data types for consistency.
#### PowerBI - Data Cleaning
- Basic data cleaning steps:
  - Convert columns to proper data types (e.g., Whole Number).
  - Format text (e.g., UPPERCASE for uniformity).
  - Rename columns for clarity.
  - Remove unnecessary data (e.g., specific values or categories).
#### PowerBI - Data Formats in Power BI
- Field types and symbols:
  - **Σ (Sigma)**: Indicates a numerical or summable field.
  - **Calendar Icon**: Represents a date field, useful for time-based analysis.
#### PowerBI - DAX Language
- **DAX (Data Analysis Expressions)**: Formula language for creating measures and columns.
  - **Example**: `GrossTotal = SUM(financials[Gross Sales])` sums up values in the "Gross Sales" column.
  - Functions similar to Excel but more powerful in modeling and calculations within Power BI.
#### PowerBI - Adding Measures and Tables
- **New Measure**: Creates calculated fields based on existing data.
  - Example: `Total Units Sold = SUM(financials[Units Sold])`
- **New Table**: Use DAX to create new tables.
  - Example: `Calendar = CALENDAR(DATE(2013,01,01), DATE(2014,12,31))`
#### PowerBI - Creating the Data Model
- **Purpose**: Organize and relate data tables.
- **Steps**:
  - Establish relationships between tables, e.g., `Financials` table linked to `Calendar` table via `Date` column.
- **Image of Data Model**:

![Pasted image 20241026145631.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/69369116f2e8048f04f6084e16014bd352af3893.png "wikilink")

#### PowerBI- Creating the Visuals
- **Steps to Add Visuals**:
  - Select a visual type from the Visualizations pane.
  - Drag it onto the report workspace.
  - Add fields from Data pane to the selected visual.
  - Additional customization options are available at the bottom of the pane.
- **Example Visuals**:
  1. **Executive Summary Title** (Label).
  2. **Profit by Date** (Line chart).
  3. **Profit by Country** (Map).
  4. **Sales by Product and Segment** (Bar chart).
  5. **Date Hierarchy** (Filter).
- **Image of Visualization Dashboard**:

    ![Pasted image 20241026145507.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/19c412686f84b390d6aee119d2f6bdbba1fa6d3c.png "wikilink")

## Programming and PowerBI
-**Power BI Desktop** allows custom visuals and calculations using R or Python code.
 - This extends beyond built-in capabilities for advanced tasks.
- **Programming Languages**: R and Python
  - Frequently used for data analysis and visualization.
  - Common libraries: `matplotlib` for Python, data frames for data manipulation.
- **Advanced Analytics**
  - Custom calculations, e.g., correlation coefficients, machine learning.
  - Allows greater customization but requires knowledge of coding.
- **Data Cleaning & Wrangling**
  - Using code enables more complex data preparation than Power Query Editor.
  - Code-generated datasets in Power BI are treated similarly to ones created in Power Query Editor.
- **Visualization Options**
  - Use libraries like `matplotlib` and `seaborn` in Python for more customization.
  - **Limitation**: These are static; Power BI must capture the output for use.
- **Practical Considerations**
  - R and Python interpreters and required packages must be installed to use within Power BI.
  - Potential compatibility issues (e.g., Python 2 vs Python 3).
  - Easier to manage with Power BI Online.
- **Example with R**
  - Building simple visuals using R script within Power BI.
	  - **Example R Script Correlation Plot with PowerBi**
	  ![Pasted image 20241026162311.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/1d24481b7bc17feb31f53a1182c59220be81cd49.png "wikilink")
  - Basic code supplied for practicals.
#### Programming and PowerBI - Correlation Options
- **Purpose**: Customize `corrplot` in R for visual appearance of correlation plots.
- **Important Note**: Refresh required after each change in options.
- **Code Examples**:
  - Basic circle plot:
    ```r
    corrplot(corr_matrix, method = "circle", type = "upper", tl.srt = 0)
    ```
This creates a basic correlation plot with circles in the upper half of the matrix.
Example of basic circle plot on 'mtcars' - Motor Trend US Magazine:

![Pasted image 20241026163107.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/152e278c2b374e568a8ff6740532daf80f17d20b.png "wikilink")

  - Ordered circle plot with hierarchical clustering:
    ```r
	corrplot(corr_matrix, method = "circle", order = "hclust", addrect = 2)
    ```
 This plot orders the correlation matrix using hierarchical clustering and adds two rectangular groups.
 Example of ordered circle plot on 'mtcars' - Motor Trend US Magazine:
 
 ![Pasted image 20241026164725.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/2b95b5e5b9910fc66ee57b0cab366e85fd208ac9.png "wikilink")

  - Color method with customization:
```r
corrplot(corr_matrix, method = "color", tl.cex = 0.6, tl.srt = 45, tl.col = "black")
```
This uses colored squares instead of circles, with the text labels resized and rotated at a 45-degree angle.
Example of ordered circle plot on 'mtcars' - Motor Trend US Magazine:

![Pasted image 20241026170839.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/cdc59d70723d0c121ccd17897289a8e5aa67e0ae.png "wikilink")

  - Ellipse method with upper half display:
```r
corrplot(corr_matrix, method = "ellipse", type = "upper", tl.cex = 0.6, tl.srt = 45, tl.col = "black")
```
This plot uses ellipses in the upper half of the correlation matrix to represent the strength and direction of correlations.

![Pasted image 20241026170946.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/15375030cc11fe0c65325dda3a32a2de2c02ed38.png "wikilink")

#### Programming and PowerBI - Binary Variables and Correlation
- **Binary Variables**: Limited variability (values either `0` or `1`) reduces the statistical relevance of correlations.
- **Alternative Visualization**: Use bar charts to compare other values for binary groups, as it provides more meaningful insights.
#### Programming and BI - Dummy Variables (Categorical)
**Definition**: Dummy variables convert categorical data into a binary format (0s and 1s), making it usable in numerical analyses like correlation and regression.
##### Why Use Dummy Variables?
- Makes categorical data compatible with numerical analysis.
- Essential for analyses like **correlation** and **regression**.
##### Steps to Create Dummy Variables in Power Query:
1. **Select the Categorical Column**:
   - Example: A "Region" column with categories like "North," "South," "East," and "West."
2. **Use the "Pivot Column" Feature**:
   - Go to the **Transform** tab and click **Pivot Column**.
   - Select a **Value** column if needed, or leave blank for a binary outcome.
3. **Result**:
   - Power Query creates new columns for each category (e.g., "Region_North," "Region_South").
   - Each column will have **1** if the category applies to the row and **0** if it doesn’t.
### PowerBI - Data Connection Types
#### PowerBI - Imported Data vs Connected Data
**Imported Data**:
  - Provides a "snapshot in time" with data that resides locally (e.g., a spreadsheet).
  - Useful for static reports where data changes are controlled by the user.
  - Example: Monthly sales report saved on a local system.
**Connected Data**:
  - Comes from a remote system, allowing for real-time or periodic updates.
  - Refreshes dashboard automatically as source data updates.
  - Useful for dynamic reporting where data changes frequently.
  - Example: A live feed of stock prices updating every minute.
#### PowerBI - Uses for Connected Data
- **Sensor Systems**:
  - Monitors environmental factors or events using IoT (Internet of Things).
  - Example: Sensors tracking weather, road traffic, or customer presence in stores.
- **Traditional Systems**:
  - Data from systems like cash registers or stock exchanges can connect directly to dashboards or be aggregated first.
  - Example: MySQL database with sales data connected for daily reporting.
#### PowerBI - Why Not Always Use Connected Data?
- **Real-time Decision Making**:
  - Connected data supports quick decision-making for short-term goals.
  - Example: Adjusting staffing levels based on real-time customer traffic data.
- **Complexity and Risks**:
  - Increased complexity with potential issues if data source fails.
  - May need data transformation to fit dashboard requirements.
#### PowerBI - Things You Can Connect To
- **Various Data Sources**:
  - Power BI integrates with multiple data sources for dashboard and report generation.
  - Examples include Google Analytics, SQL databases, Azure services, and Excel workbooks.
**PowerBI - Data Source Connections**:

![Pasted image 20241026194817.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/ef9f118deab210f075f2f624d8577faf810e969b.png "wikilink")

### PowerBI - Spatial Data
##### PowerBI - Spatial Data
- **Spatial Data Importance**: Data often includes a location attribute with additional properties.
  - **Quantitative Example**: Latitude and longitude.
  - **Categorical Example**: Country, state, city, campus, or building.
- **Utility of Spatial Data**: Enhances analysis by adding context and comparisons across locations.
#### Revision: Spatial Data Types
- **Point**: Represents a single location without area.
  - *Example*: UWA Business School at 31.9859 S, 115.8207 E.
- **Polygon**: Represents a shape with area, composed of multiple lines.
  - *Example*: Coastline boundaries of Australia or UWA.
- **Line**: Consists of multiple points, often used to represent roads.

![Pasted image 20241026204409.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/470c7113404c14561cecb3c2b34917e11c37c19f.png "wikilink")

#### Spatial Operations
- **Common Operations**:
  - **Topological**: Checks if areas intersect, are disjoint, or touching, and measures distances.
  - **Joining**: Associates points with polygons (e.g., which stores are in a country) and identifies nearby points.
- **Most Descriptive Data**: Polygons are highly descriptive and support rich analysis.
#### Spatial Operations (Part II)
- **Further Operations**:
  - **Raster Data**: Used for pattern recognition in images.
  - **Advanced Distance-Based Operations**: More complex spatial analysis.
  - **Aggregation**: Combines smaller areas into larger, sometimes leading to issues.

![Pasted image 20241026204545.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/ef302dc98a1182fd3510e4cd27f2e107fc0fb5e6.png "wikilink")

#### More Spatial Considerations in BI
- **Advanced Use of Spatial Data in Power BI**:
  - **Point-based Data**: Preferred over categorical country-based data.
  - **Hierarchical Analysis**: Drill down between regions within a country.
  - **Choropleth Maps**: Color-shaded maps for better data representation.
- **Visual Sources**: Some visuals require third-party sources (e.g., Mapbox, ESRI) or script visuals.
#### Spatial Visualisations - Adjusting the Map
- **Practical Conversion**: Transform bubble maps into filled (choropleth) maps.
  - **Improves Comparison**: Highlights differences between countries.
  - **Color Choice**: Select noticeable color scales.
  - **Accuracy**: Ensure visuals do not misrepresent data; account for colorblind accessibility.
### Business Intelligence/PowerBI-  Data Workflow
- **Definition**: A data workflow is a series of tasks to process data.
- **Variation**: Workflows vary by project goals and dataset content but share common steps.
- **Application in BI**: Commonly used in BI for generating reports and dashboards.
#### Business Intelligence Workflow
**Steps**:
  - **Problem Identification**: Define the question and intended audience.
  - **Data Acquisition**: Collect relevant and fit-for-purpose data.
  - **Data Preparation**: Clean, transform, and structure data.
  - **Data Analysis**: Perform analysis to derive insights.
  - **Visualization & Reporting**: Present findings in a clear format.
- **Note**: Most time is spent in the first three steps.
#### BI Workflow - Problem Identification
- **Purpose**: Establish clarity on objectives and audience.
- **Quote**: "Failure to plan is planning to fail." – Benjamin Franklin
- **Considerations**:
  - What is the question we want to answer?
  - Who will use the dashboard or report?
#### BI Workflow - Problem Statement
- **Purpose**: Clearly define the problem and target audience.
- **Example**: "I am interested in the average daily percentage change of stock prices for Microsoft, Apple, and Amazon."
- **Outcome**: Helps identify necessary data, analysis methods, and presentation format.
#### BI Workflow - Data Acquisition
- **Goal**: Gather data that is relevant to the problem.
- **Key Questions**:
  - What are the important considerations when acquiring data?
  - How does the "who" in the problem statement impact data choices?
#### Data Acquisition – Theoretical Issues
- **Data Source**: Is it trustworthy and authoritative?
- **Metadata**: Is there a description provided?
- **Standards**: Does it follow a recognized format?
- **Relevance**: Does it help solve the identified problem?
- **Licensing**: Consider costs, time, and legal aspects.
- **Currency**: Is the data up-to-date?
- **Accuracy**: Is it reliable for our purpose?
- **Recording Method**: How is data collected (e.g., time series)?
- **Format Compatibility**: Is it compatible with our tools?
- **Connection Type**: Is it imported or connected?
#### Data Acquisition – Practical Issues
- **Data Size**: Is it manageable?
- **Transferability**: Can it be sent over the internet?
- **Generation Time**: How long does it take to be produced?
#### BI Workflow - Data Preparation Challenges
### Data Preparation Challenges in BI
1. **Missing Data**: Some values are absent from the dataset, which can impact analysis accuracy.
   **Example**: A customer table lacks "Email" entries for some customers, affecting communication analyses.
2. **Incorrect Formats**: Data is in a format that's incompatible with analysis or visualization needs.
   **Example**: Dates entered as text ("2024-October-29") instead of a standard date format.
3. **Inconsistencies**: Variations in data entry or naming, causing mismatches.
   **Example**: A "Country" column has entries like "USA," "United States," and "U.S.", which should be standardized.
4. **Need for Normalization or Enrichment**: Data may need scaling (normalization) for consistency or external information (enrichment) for context.
   **Example**: Normalizing income data to the same currency or adding population data to a city table.
5. **Irrelevant Data**: Data that does not contribute to the analysis goal and may clutter or confuse results.
   **Example**: A customer table includes "Favorite Color," which is irrelevant to sales performance analysis.
#### BI Workflow Evolution - ETL vs. Data Preparation
- **ETL**: Stands for Extract, Transform, Load.
- **Components**: Data transformation and cleaning.
- **History**: Linked with data warehousing for 50+ years.
- **Distinction**: ETL is related to data warehouses but serves different functions.
**ETL (Extract, Transform, Load)**: A method for data acquisition and preparation.
  - **Extract**: Get data from the source.
  - **Transform**: Format data for the destination.
  - **Load**: Import data into the destination system.
- **Abstract Process**: Models dashboard/report building in Power BI.
#### B Workflow - Data Analysis
- **Goal**: Answer initial problem using various techniques.
- **Integration with Power BI**: Analysis links closely with visualization.
- **Steps**:
  - **Exploratory Data Analysis (EDA)**: Descriptive stats and visuals for a preliminary understanding.
  - **Detailed Analysis**: Move to deeper insights after EDA.
#### BI Workflow - Data Analysis Activities
- **Get Value**: Find specific values (e.g., today’s closing price).
- **Filter**: Select data by criteria (e.g., products sold > 500 units).
- **Derive Value**: Calculate metrics (e.g., average CTR).
- **Find Extreme**: Identify max/min values (e.g., top salesperson).
- **Sort**: Arrange data by specific metric (e.g., ASX200 by profit).
- **Find Range**: Determine min and max values across data (e.g., revenue range).
- **Distribution**: Calculate metrics like mean and standard deviation.
- **Anomaly Detection**: Identify outliers (e.g., developer with highest code lines).
- **Clustering**: Group data by similarity (e.g., hours worked clusters).
- **Correlation**: Analyze relationships between variables (e.g., productivity vs. remuneration).
- **Contextualization**: Use data to provide location-based insights (e.g., bus routes for meetings).
#### MECE Principle
- **Purpose**: Ensure data quality and completeness.
  - Data should be **Mutually Exclusive** and **Collectively Exhaustive**.
- **Implementation**: McKinsey method to divide problems into smaller parts.
#### MECE Example
- **Scenario**: Business selling 10 products with data on profit and stock levels.
  - **Profit**: Sum of mutually exclusive profits of each item.
  - **Stock**: Sum of mutually exclusive stock levels of each item.
- **Use Case**: Drill up/down data to simplify or elaborate as needed.
#### Other Things We Can Do With Data
- **Beyond Visualizations**:
  - **Derived Data Sets**: For further analysis.
  - **Mathematical Models**: Advanced analysis (e.g., algorithms).
- **Iterative Process**: Begin with simple analysis, increase complexity, add data sources over time.
### PowerBI - Data Visualisation
**Purpose**: Present results to the target audience in an understandable way.
- **Considerations**:
  - Avoid confusing fact with opinion; let the data tell the story.
  - Avoid misrepresenting data by:
    - Using correct visualization types.
    - Ensuring properly labeled axes.
    - Avoiding unusual axes or selective data representation.
#### BI Visualisations - Types of Visualisation Content
- **Time Series**: Shows changes over time.  
  *Example*: GDP per quarter since 1972.
- **Order/Ranking**: Shows order from largest to smallest or alphabetically.  
  *Example*: Products ranked by total sales volume.
- **Partition**: Represents parts of a whole, often in percentages.  
  *Example*: Sales percentage by country.
- **Deviation**: Shows differences between planned and actual.  
  *Example*: Budget vs. actual expenditure in a business unit.
#### BI Visualisations - Additional Data Visualisation Types 
- **Frequency**: Shows how often a quantity occurs.  
  *Example*: Store visitors per hour.
- **Correlation**: Compares two variables to find relationships.  
  *Example*: Hours worked vs. GDP.
- **Comparison**: Compares categorical data across groups.  
  *Example*: Sales per sales channel.
- **Geospatial**: Represents data across physical locations.  
  *Example*: Employees per building floor.
#### BI Visualisations - Types of Visualisations in Power BI
- **Common Types**: Bar, column, line, scatter, and map.
- **Choice Depends on Data**: Select appropriate visualizations based on the data being represented.
#### BI Visualisations - Drilling Up and Down

![Pasted image 20241026223900.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/87d9542ea39457a7b7de1194d46bb2eae870d0f6.png "wikilink")

- **Slicers**: Allow detailed or aggregated data views.
- **Requirements**: Data should be mutually exclusive for effective slicing.
- **Note**: Some visualizations may not strictly appear as charts but still provide functional insights, such as slicers.
#### Useful Actions in Power Query with Loaded Data
- **Data Transformation**:
  - Change data types, rename columns, and reorder rows or columns to prepare data for analysis.
- **Data Cleansing**:
  - Remove duplicates, filter out nulls, and perform conditional replacements to improve data quality.
- **Merge and Append Queries**:
  - Combine multiple tables with `Merge` (joins tables side by side) or `Append` (stacks tables vertically), useful for datasets split across sources.
- **Column Splitting and Grouping**:
  - Split columns by delimiters, positions, or patterns to reorganize complex data.
  - Group data based on specific columns, with aggregate functions (like sum, average) for summarization.
- **Custom Columns and Calculated Fields**:
  - Add custom formulas to create calculated columns or new measures tailored to the problem, improving data relevance and usability.
### PowerBI Project
#### PowerBI Project - MySQL and Power BI
- **Dashboard Setup:**
  - Create a new project in Power BI Desktop.
  - Select “Get Data” → “MySQL database” → Connect.
  - **Server:** `db.tris.id.au`
  - **Database:** `<YourStudentID>_db` (replace with your student ID).
- **Issues:** MySQL connector may have issues; focus on understanding the process rather than troubleshooting connection errors.
#### PowerBI Project - Brief (for the Practical)
- **FAANG Companies:** Main players in ‘big tech’:
  - **F:** Meta (Facebook) - `NASDAQ:META`
  - **A:** Amazon - `NASDAQ:AMZN`
  - **A:** Apple - `NASDAQ:AAPL`
  - **N:** Netflix - `NASDAQ:NFLX`
  - **G:** Alphabet (Google) - `NASDAQ:GOOG`
#### PowerBI Project - Polygon API Key
- **API Setup:** 
  - Register on [Polygon.io](https://polygon.io/dashboard/signup) to obtain an API key.
  - **Purpose:** Connects Power BI to live stock data using REST API.

![Pasted image 20241029171319.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/dc88b7cd1fb55509003a05e0a7eba404c441df73.png "wikilink")

#### PowerBI Project - Connecting the Data
- **Connection Process:**
  - Use “Get Data” → “Web” in Power BI.
  - API endpoint format: `http://api.polygon.io/v1/open-close/` + `Stock Code` + `/Date` + `?adjusted=true&apiKey=YourAPIKey`.
#### PowerBI Project - Generalising the Data
- **Parameter Setup:**
  - Use “Manage Parameters” to create parameters for “StockCode” and “DatePart.”
  - Stock codes: META, AMZN, AAPL, NFLX, GOOG.
#### PowerBI Project - Creating Functions
- **Data Transformation:**
  - Use **Convert** to format queries as tables.
  - Use **Transpose** and **Use First Row as Headers** to arrange data.
- **Data Shape:** 

![Pasted image 20241026225802.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/e713201b50f4798ffed39122813f65edcd5b744e.png "wikilink")
#### PowerBI Project -  Creating Tables
- **Tables Required:**
  - **Stocks Table:** Contains stock codes (e.g., META, AMZN, AAPL).
  - **Dates Table:** Contains dates in `YYYY-MM-DD` format.
  - Ensure both columns are in **Text** format.
#### PowerBI Project - Real-World Problems
- **Errors and Solutions:**
  - Free service API may cause data request errors if queried too quickly.
  - Retry requests; expanded columns will display correctly.
  - Rename expanded columns and the query/table as needed.
#### PowerBI Project - Creating Report
- **Report Creation:**
  - Use appropriate visuals for each dashboard element.
  - **Considerations:** Improve data presentation; avoid misleading visuals.
  - Answer any related questions from the brief.
#### Power BI Parameters
**Parameters in Power BI**: Variables that store values, allowing flexibility and customization in reports.
  - Can be used to dynamically change data sources, filter data, or adjust queries without modifying the underlying code.
**Using Parameters with APIs and JSON Queries**:
- **API Integration**: Parameters can be used to pass values directly into API URLs, making it easier to query endpoints with dynamic filters, dates, or locations.
- **JSON Queries**: Parameters can specify key values (e.g., `date`, `region`) in JSON queries, enabling dynamic data retrieval from JSON APIs.
**Data Acquisition Relevance**:
- **Data Size**: Parameters allow filtering large datasets at the API level, reducing data size before import.
- **Currency**: Ensures up-to-date data is fetched by allowing date-based parameters for recent records.
- **Transferability**: Minimizes data transferred over the internet by focusing only on relevant data.
- **Accuracy and Relevance**: Ensures only relevant data to the problem is retrieved by configuring API queries through parameters.
### Other Types of Databases
**Main Difference between NoSQL Databases and Relational Databases**
  - NoSQL databases lack a fixed schema; each observation (record) can vary in structure.
  - **Example**: MongoDB stores data in flexible documents, allowing each document to have different fields.
**Difference between Document Databases and Relational Databases**
  - Document databases store data in multiple, queryable "documents" rather than tables.
  - **Example**: In MongoDB, each document in a collection can store data of varying formats and structures.
- **Document Database as NoSQL**
  - Document databases are typically NoSQL, but NoSQL databases are not limited to document storage.
  - **Example**: A key-value store (Redis) is also NoSQL but is not a document database.
- **When to Use a Graph Database**
  - Graph databases are used when relationships between data elements are essential.
  - **Example**: Neo4j is ideal for social networks where connections between users are key to data organization.
### MongoDB
#### MongoDB Collections and Documents
**Collection**: A **collection** is a grouping of MongoDB documents, similar to a table in relational databases.
- **Characteristics**: Collections store documents with flexible schemas, allowing different fields and data types within the same collection.
**Document**: A **document** is a record in MongoDB, represented as a JSON-like structure (BSON), similar to a row in relational databases.
- **Structure**: Contains **key-value pairs** (e.g., `{ id: 1, name: "Widget", price: 99.99 }`), where each document can have a unique set of fields.
#### Creating Data in MongoDB
- **Creating a Collection**
  - Command: `db.createCollection("<CollectionName>")`
- **Inserting Documents**
  - Command format:  
    `db.<CollectionName>.insert({attribute: value, ...})`
  - **Multiple Insert**:  
    Use `insertOne` for single documents, `insertMany` for arrays of documents.
- **Example Insertion Command**
  ```plaintext
  db.transactions.insert({
      id: 1,
      description: "Basic Widget",
      quantity: 1,
      unitPrice: 123.45,
      totalPrice: 123.45,
      hasGst: true
  })
  ```
#### Querying Data in MongoDB
- **Finding Documents**
  - `.find()` retrieves documents in a collection.
  - Full format: `db.<CollectionName>.find().pretty()`
- **Simple Queries**
  - Example: `.find({id: 1})` returns documents with `id` equal to 1.
#### Inequalities with MongoDB
- **Inequality Keywords**
  - `$lt`: Less than
  - `$lte`: Less than or equal to
  - `$gt`: Greater than
  - `$gte`: Greater than or equal to
  - `$ne`: Not equal to
- **Example**:  
  `.find({attributeName: {$lt: 1}})` finds documents where `attributeName` is less than 1.
#### 'In' Queries using MongoDB
- **In-Type Queries**
  - `$in`: Values within a specified list.
  - `$nin`: Values not in a specified list.
- **Example**:  
  `.find({attributeName: {$in: [1, 2, 3]}})` finds documents where `attributeName` is 1, 2, or 3.
#### Querying Data in MongoDB
- **Query for items in the "transactions" collection**:
  - **Unit price less than $100**: `db.transactions.find({ unitPrice: { $lt: 100 } }).pretty()`
  - **Items without GST**: `db.transactions.find({ hasGst: false }).pretty()`
  - **Quantity greater than 1**: `db.transactions.find({ quantity: { $gt: 1 } }).pretty()`
  - **Exclude item with ID of 3**: `db.transactions.find({ id: { $ne: 3 } }).pretty()`
- **Using `.pretty()`** makes the output formatted and readable.
#### Example MongoDB Query
- **Query format example**:
  - `db.transactions.find({ someVal: { $ne: false } }).pretty()`
    - This searches the `transactions` collection for documents where `someVal` is not equal to `false`.
    - Output is made readable using `.pretty()`.
- **Note**: More advanced queries are possible by combining the above constructs.
### Graph Databases
- **Concept**  
  - Based on the mathematical concept of a graph.
  - A **graph** consists of:
    - **Nodes**: Represent entities (e.g., people, movies).
    - **Edges**: Represent relationships between nodes (e.g., directed connections).
  - Both nodes and edges hold data.
    ![Pasted image 20241026231900.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/25c4d2e1dd31e3d9ece58faeab03944572cccb70.png "wikilink") - *Graph with nodes and edges illustrating relationships (Example includes nodes like movies and people)*
#### Creating a Graph Database
- **Software Options**
  - Various graph database software can be used (e.g., Neo4j).
  - Typically involves loading data from CSV files and mapping rows to entities and relationships.
- **Example** (Marvel scenario)
  - Load and create **Person** nodes (ID, Name).
  - Load and create **Movie** nodes (ID, Name, Budget).
  - Define **"Directed"** relationships between persons and movies.
  - Define **"Acted In"** relationships between persons and movies.
#### Querying a Graph Database
- **Basic Queries**
  - **MATCH (n) WHERE n:Person OR n:Movie RETURN n** – Retrieves all nodes labeled as Person or Movie.
- **Relational-Style Query**
  - **MATCH (m:Movie {name: "captain america"}) RETURN m** – Finds a movie by name.
- **Relationship-Based Query**
  - **MATCH m=(p:Person {name: "anthony russo"})-[:Directed]->(n) RETURN m** – Finds all movies directed by Anthony Russo.
#### Graph Database Software
- **Differences in Software**
  - Some are open-source (e.g., Neo4j), while others are paid.
  - Query languages may vary:
    - **Cypher** (e.g., Neo4j).
    - **SPARQL** for other types.
  - Data representation varies (e.g., RDF, Turtle).
- **Challenges and Developments**
  - Traditionally complex setup and lower performance; improvements have been made.
  - Related technologies include **Blockchain** due to the nature of interconnected data.
### Non-Technical Issues
#### Non-Technical Issues - Security, Ethical, and Privacy Issues
- **Data Gathering in Business**
  - Data is collected from customers for products/services.
  - Legal requirements (e.g., AML/CTF) may necessitate data collection.
- **Data as an Asset**
  - Data is powerful, often immutable, and not "owned" by anyone.
  - Certain data cannot be changed, and disclosure has significant impact (e.g., personal identification, health info).
  - "Owned" data may be changeable but risky if leaked (e.g., corporate data in espionage).
#### Non-Technical Issues - Security Issues
- **Unprotected Systems**
  - Unprotected systems can expose data to unauthorized access.
- **Prevention Methods**
  - Use strong usernames, passwords, or other authentication.
  - Assign minimal permissions to groups, especially with internet access.
  - Regularly update software to patch vulnerabilities.
  - Enable audit logs and other technical solutions to trace issues if they occur.
#### Non-Technical Issues - Ethical Issues
- **Improper Use of Data**
  - Data used without consent can be ethically questionable.
- **Examples**
  - **Targeted Advertising** - Based on behavior; limited surveillance.
  - **Health Predictions** - Insurances using personal data to predict outcomes.
  - **Automated Stereotyping** - Data profiling creating digital stereotypes.
  - **Unauthorized Data Use** - Selling data to third parties without consent.
  - **Email Spam** - Anti-spam laws offer some protection but not always effective.
#### Non-Technical Issues - Privacy Issues
- **Data Privacy**
  - Data should remain private and used only as agreed.
- **Privacy Erosion Risks**
  - Legitimate data use can lead to fraud or embarrassment if leaked.
  - Technical and social controls are necessary to ensure data privacy.
- **Consumer vs. Business Privacy**
  - Privacy issues impact consumers and business-to-business contexts.
  - Intellectual property and trade secrets are vulnerable to corporate espionage.
## Non Technical Issue Case Studies - Analysis Method
Activity involves group discussions on real-world case studies about privacy, ethics, and security issues in data handling.
**Questions to consider for each case:**
  - **What happened?** (e.g., data that was leaked)
  - **Who was affected?** (individuals, groups, organizations)
  - **Why is this a problem?** (identify the issues involved)
  - **How could this be prevented in the future?**
  - **Can any non-monetary remediation be offered?**
#### Case Study Examples
##### Myki Leak
- **Scenario:** Victorian Government released transaction data from the Myki ticketing system as part of a hackathon.
- **Outcome:** Researchers linked data with public tweets, identifying travel patterns of politicians.
- **Issues:** Privacy breach due to potential identification of individuals.
- **Prevention:** Implement stronger anonymization protocols.
##### Mailing List
- **Scenario:** Jim purchased a product and provided an email for the invoice.
- **Outcome:** Jim was automatically added to a mailing list without consent.
- **Issues:** Violation of consumer consent and privacy.
- **Prevention:** Obtain explicit consent for mailing list subscriptions.
##### Optus "Hack"
- **Scenario:** Optus exposed personal details of up to 9.8 million customers.
- **Outcome:** ID numbers and other personal information were leaked.
- **Cause:** Likely through an unauthenticated API.
- **Issues:** Significant privacy and security breach, affecting many individuals.
- **Prevention:** Implement authentication and authorization for APIs.
##### Job Application
- **Scenario:** AI was used to determine suitable candidates for a job position.
- **Outcome:** Qualified candidate, Jane, was denied due to algorithmic bias.
- **Issues:** Ethical issue due to bias in AI decision-making based on gender.
- **Prevention:** Regular audits and transparency in AI algorithms.
### Distributed Databases
#### Blockchain
- **Definition**: A distributed, immutable ledger of transactions.
  - **Distributed**: Source of truth is shared across multiple nodes (machines).
  - **Immutable**: Transactions are permanent and cannot be changed.
  - **Ledger of Transactions**: A standardized record of operations.
- **Use Cases**
  - Primarily used in **Cryptocurrency**, **NFTs**, and **Smart Contracts**.
  - Suitable for problems requiring:
    - Decentralization (no single point of failure).
    - Transparency and trust (immutable history).
  - Example: **Bitcoin** uses blockchain to securely record transactions without a central authority.
# Lab 1
## Business Intelligence Concepts
### 1. What are the 5 Types of Analytics?
#### 3 Primary Types of Analytics
1. **Descriptive** - Describes what happened in the past. 
   e.g. report showing sales performance for last quarter
2. **Predictive** - Predicting what is likely to happen in the future.
   e.g. Sales revenue for next quarter is likely to increase by 5% compared to last quarter due to historical trend of increasing sales on average by 5% quarter on quarter.
3. **Prescriptive** - Suggests how we can make outcomes happen in the future.
   e.g. deploy new marketing promotion this month to ensure sales revenue next quarter increases by 5%.
#### 2 Further Types of Analytics:
4. **Diagnostic** - Helps explain why something happened in the past.
   e.g. sales increased last quarter due to higher lead to customer conversion last quarter because of more targeted marketing and lead engagement.
5. **Comparative** - comparing two different things in the same way. Typically combined with diagnostic analytics to find out similarities and differences (why the sales revenue differ).
   e.g. comparing sales revenue from two different states to find out which region performed better.
## 2. Is the Human Factor of BI development important?
Yes there are two sides to the human factor one is the business or data analyst whose job it is to ensure that the data is captured processed and transformed correctly. The other end of the spectrum is the users who use the analytics reports, the insights, whether they are visualizations or reports need to be of value. Usually they should either support, influence or help in the decision making process.
- **Human insight drives relevance**: Business users understand the context and goals, ensuring that BI tools provide meaningful insights for decision-making.
- **Interpretation of data**: While automated tools analyze data, human intuition is crucial for interpreting results, spotting anomalies, and applying insights to real-world scenarios.
- **Customization and flexibility**: Humans can tailor BI systems to evolving business needs, ensuring adaptability in dynamic environments.
- **Preventing bias and errors**: The human factor helps identify and mitigate biases in data collection, analysis, and interpretation that machines may overlook.
- **Effective communication**: Data storytelling and conveying insights to diverse stakeholders require human skills for clarity, persuasion, and actionable recommendations.
- **Facilitating adoption**: Human involvement in development and training helps ensure that BI tools are user-friendly and widely adopted within the organization.
- **Ethical oversight**: Humans play a critical role in ensuring ethical use of data, guarding against misuse or misinterpretation of sensitive information.
#### 3.1 What are the different types of visualizations?
**Definition:** A way to display data. e.g. Bar chart, waterfall chart, scatter plot
### Visualizations - Types
- **Bar Chart**: Compare values across categories; easy to interpret differences.
- **Line Chart**: Track changes or trends over time.
- **Pie Chart**: Show parts of a whole; limited to simple compositions.
- **Heatmap**: Visualize data density and distribution across dimensions.
- **Scatter Plot**: Show relationships or correlations between two variables.
- **Histogram**: Display data distribution and frequency.
- **Tree Map**: Show hierarchical data and part-to-whole relationships.
- **Gauge Chart**: Represent progress towards a goal or key performance indicator (KPI).
- **Pivot Table**: Summarize data interactively across multiple dimensions.
- **Map Chart**: Geographically visualize data, such as regional performance.
#### 3.2 How do you select and decide on a visualization?
Selecting and designing visualization depends on multitude of factors:
1. **Type of data**
2. **What we want to communicate**
3. **Level of data (drill up, drill down, drill through)**
4. **Aesthetic considerations e.g. colour**
E.g. Situation: Data analyst working for e-commerce company. Sales data for different product categories across multiple regions, goal is to create dashboard for senior management to review monthly performance.
1. **Type of Data available** - Numerical (Sales figures), Categorical (Product Categories) , Geographical (Regions), and Time Period (Monthly)
2. **What we want to communicate** - Objectives: Overall monthly sales trends, Sales performance comparison across different regions, Identify top-performing product categories, Provide option to drill down into specific regions/categories for detailed analysis
3. **Consider level of data** -  **Drill up:** Overview of total monthly sales, **Drill down:** detailed analysis by region/product category, **Drill through:** Further exploration to see individual transactions or customer demographics
4. **Aesthetic Considerations** - Use brand/product colours to differentiate product categories. Choose consistent colour palette for different regions. Ensure charts and graphs aren't overcrowded. Use labels and legends for clarity.
### 4. Give an example of how data can be dilled up/down?
Lets take the example of a revenue dashboard in PowerBI for a car sales dealership. We could have the revenue dashboard across the business (the highest level of the visualisation), then we could drill down to see revenue by segementation for example if it’s in Australia we could show the revenue by the state, if we drill down further we could drill down all the way.
**Bigger picture = drill up**
**Details = drill down**
**Data Drilling:** Looking at different components of data in different ways - **interrogating data.**
- **Drilling up/Drilling down:** Explore next level down/up of detail. Done first in DBMS.
- **Drill through:** select part of visual and be taken to another page in report. Filtered to data that relates to part selected on original page.
- **Filter:** Removes data that doesn't apply. Conversely, <u>highlight greys</u> out data that doesn't apply.
### 5. How do you connect to the database in MySQL Workbench?
1. Open **MySQL Workbench**.
2. Click the **‘plus’ button** to create a new connection.
3. In the **Connection Name** field, type a name of your choice (e.g., "TestDB").
4. In the **Hostname** field, enter: `db.tris.id.au`.
5. In the **Username** field, enter: `test`.
6. Leave the other fields blank.
7. Click **OK** to save the connection.
8. In the main window, click the new connection **tile** (the one you just created).
9. When prompted for a password, enter: `test123!`.
10. Click **OK** again to proceed.
11. If connected successfully, you will see connection information displayed.
12. To exit, press the **‘X’ button** to quit MySQL Workbench.
**MySQL Workbench**: A visual tool for database architects, developers, and administrators to design, develop, and manage MySQL databases.
**Importance**:
  - **User-friendly interface**: Simplifies database management with a graphical interface, reducing the need for manual SQL commands.
  - **Integrated tools**: Combines data modeling, SQL development, and database administration into one platform.
  - **Efficient workflow**: Enhances productivity by allowing users to perform tasks like designing databases, running queries, and managing users in one place.
  **Normal Usage**:
  - **Database design**: Create and modify database schemas using visual modeling tools.
  - **SQL development**: Write, execute, and optimize SQL queries through an integrated editor.
  - **Database administration**: Manage users, backups, server configuration, and data import/export.
  - **Performance tuning**: Monitor and optimize database performance with built-in analysis tools.
  - **Migration**: Support for migrating databases from other platforms to MySQL.
# Lab 2
## Database Concepts
### 1. What makes a database a database?
**Database definition:** Allows us to store, retrieve, change, and analyze data in a structured format. It is an organized collection of data stored in a consistent manner. There are many different types of database, an example of a database is MySQL which is relational database.
### 2. What are the vital components of a database?
1. **Entities:** something we store data about, represented by its properties
2. **Properties:** define what makes an entity unique and how to describe it.
	e.g Person entity has properties FullName, EmailAddress, BirthDate
### 3. How do we know something isn’t a database?
To determine if something is not a database it will have these properties:
1. **Lack of structure:** No organized structure like tables, rows, columns, or defined data schema
2. **No Querying Mechanism**: Lacks tools (like SQL) for data retrieval, filtering, and manipulation
3. **No concurrency Support**: Cannot support multiple users querying/interacting with data at same time
4. **No access control**: Doesn't offer fine-grained access controls for managing security and user permissions.
### 4. Can databases only take one format or can they take many?
Databases can take many formats because:
1. **Different Data Structures**: Use various structures (tables, documents, key-value pairs) to suit specific data types
2. **Adaptability to Data Types**: Formats chosen based on whether data is structured, semi-structured, or unstructured.
3. **Optimized Use Cases**: Each format addresses specific needs, e.g. relational for transactions, graph for relationships.
4. **Performance Requirements**: Different formats improve performance for various tasks, like real-time analytics (NoSQL) or time-series data.
5. **Scalability and Flexibility** Some formats, like NoSQL and NewSQL offer scability and flexibility for large-scale dynamic data.
**Types of Databases:** Object-oriented, distributed, data warehouse, NoSQL, Graph, OLTP, Open-source, Cloud, Multimodal, and Document Database
### 5. Scenario: What is the most appropriate database model?
*Kim runs a financial services company that organizes peer-to-peer loans between organisations. Some of these organisations loan money to other organisations, some receive loans from other organisations and others do both of the above. Kim is not interested in storing the loan transactional data itself; this is handled by a different system, but rather for risk analysis Kim wishes to understand the relationships between  different organisations.*
**Answer**
**Graph database model** is the most appropriate choice because:
1. **Focus on Relationships**  
   - Kim needs to understand relationships between organizations—such as which ones loan to others or receive loans. Graph databases are specifically designed to model complex relationships between entities, making this analysis straightforward.
2. **Efficient Relationship Queries**  
   - Graph databases can quickly traverse relationships (e.g., borrower-lender relationships) without the need for complex joins, which makes them ideal for risk analysis and network analysis.
3. **Flexibility for Complex Network Data**  
   - Graph databases allow Kim to represent organizations as **nodes** and loan relationships as **edges** between nodes, which is perfect for visualizing and analyzing interconnected financial networks.
**Graph database** offers the best structure for managing and querying the intricate relationships central to Kim’s risk analysis.
### 6. Scenario: Design a data model for the scenario?
*Kelly runs a tree-chipping business that converts planted trees into mulch. Kelly wishes to track which sets of mulch are derived from which trees, and who it is sold to, to help with planning her business and to determine which trees are most effective. Each sale consists of a customer with an address. Each sale contains at least one batch of mulch. Each batch of mulch contains of a certain weight of tree and a certain type of tree. Each batch of mulch contains the contents of at least one tree. A tree can be in one or more batches of mulch; however, it does not need to be in a batch of mulch. Each batch has a batch code associated with it.*
a. Define the sets of entities that Kelly must store for his system
1. **Customer:** Information about customers who purchase mulch
2. **Mulch Batch**: Information on each batch of mulch produced, including trees used.
3. **Sale**: Information about individual sales transactions, includes customer details and mulch purchased
4. **Tree**: Information about trees that are processed into mulch.
b. From this, determine the Tables that are required:
1. Customer
2. Sale
3. MulchBatch
4. Tree
5. MulchBatchTree: Represent many-to-many relationship between mulch batches and trees
c. (Define and) identify the attributes required for each entity
1. **Customer**
- CustomerID (Primary Key)
- Name
- Address
- Contact Information (optional but could include email, phone)
2. **Sale**
- SaleID (Primary Key)
- CustomerID (Foreign Key from Customer)
- SaleDate
- TotalAmount (optional)
3. **MulchBatch**
- BatchCode (Primary Key)
- SaleID (Foreign Key from Sale, nullable as a batch might not be sold yet)
- Weight
- TreeType (type of tree used in the mulch batch)
4. **Tree**
- TreeID (Primary Key)
- PlantDate
- Type (type of tree, e.g., pine, oak)
5. **MulchBatchTree** (Associative entity for many-to-many relationship between MulchBatch and Tree)
- BatchCode (Foreign Key from MulchBatch)
- TreeID (Foreign Key from Tree)
d. (Define and) identify the primary and foreign keys;
1. **Customer Table**
- **Primary Key**: customerId
2. **Sale Table**
- **Primary Key**: saleId
- **Foreign Key**: customerId
3. **MulchBatch Table**
- **Primary Key**: batchCode
- **Foreign Key**: saleId (nullable)
4. **Tree Table**
- **Primary Key**: treeId
5. **MulchBatchTree Table**
- **Primary Key**: Composite Key (batchCode, treeId)
- **Foreign Key**: batchCode
- **Foreign Key**: treeId
e. Describe the cardinality of each relationship.
1. **Customer to Sale**: **One-to-Many (1:M)**
- Each `Customer` can have multiple `Sales`, but each `Sale` is associated with only one `Customer`.
2. **Sale to MulchBatch**: **One-to-Many (1:M)**
- Each `Sale` can contain multiple `MulchBatches`, but each `MulchBatch` is linked to only one `Sale`.
3. **MulchBatch to Tree**: **Many-to-Many (M:N)**
- Each `MulchBatch` can contain mulch from multiple `Trees`, and each `Tree` can be part of multiple `MulchBatches`. This relationship is represented by the `MulchBatchTree` table.
**Entity Relationship Diagram:**
![Pasted image 20241027121135.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/6c48ba5063608035058732aef2f75840b7b5159a.png "wikilink")
### 7. Scenario: Design a data model for the scenario?
*Raj runs a business selling donuts to customers. Due to demand, each transaction consists only of one donut; however that donut may differ in cost and type between transactions. For compliance reasons, Raj must store the name and email of each customer who purchases a donut and desires to know when the donut was purchased to help understand demand*
a. Define the sets of entities that Raj must store for his system
1. **Customer**: Stores information about each customer.
2. **Transaction**: Stores details of each transaction, including the donut purchased and purchase details.
3. **Donut**: Stores information about different types of donuts.
b. From this, determine the Tables that are required
1. **Customer**
2. **Transaction**
3. **Donut**
c. (Define and) identify the attributes required for each entity
1. **Customer**
- `customerId` (Primary Key)
- `name`
- `email`
2. **Transaction**
- `transactionId` (Primary Key)
- `customerId` (Foreign Key from Customer)
- `donutId` (Foreign Key from Donut)
- `purchaseDate` (Date and time of purchase)
- `price` (Price of the donut in the transaction)
3. **Donut**
- `donutId` (Primary Key)
- `type` (Type of donut, e.g., glazed, chocolate)
- `basePrice` (Standard price for each type of donut)`
d. (Define and) identify the primary and foreign keys
1. **Customer Table**
- **Primary Key**: `customerId`
2. **Transaction Table**
- **Primary Key**: `transactionId`
- **Foreign Key**: `customerId`
- **Foreign Key**: `donutId`
3. **Donut Table**
- **Primary Key**: `donutId`
e. Describe the cardinality of each relationship
1. **Customer to Transaction**: **One-to-Many (1:M)**
- Each `Customer` can have multiple `Transactions`, but each `Transaction` is associated with only one `Customer`.
2. **Donut to Transaction**: **One-to-Many (1:M)**
- Each `Donut` type can appear in multiple `Transactions`, but each `Transaction` is linked to only one specific `Donut` type.
**Entity Relationship Diagram:**
![Pasted image 20241027123844.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/ca0c1a5813726e1ea79d236058778aa322ad3474.png "wikilink")
# Lab 3
## SQL Basics
### 1. Create Entity Model for Transaction Item
**Required Columns**
**Generated Columns - Virtual (changing/not a lot of values)**
**Constraints on input (referential integrity)**
**tinyint for hasGst**
```sql
CREATE TABLE `TransactionItem` (
    `id` int NOT NULL AUTO_INCREMENT,
    `description` varchar(50) NOT NULL,
    `quantity` int NOT NULL,
    `unitPrice` float NOT NULL,
    `hasGST` tinyint(1) DEFAULT '0',
    `totalPrice` float GENERATED ALWAYS AS ((`unitPrice` * `quantity`)) VIRTUAL,
    `taxAmount` float GENERATED ALWAYS AS (((`totalPrice` * hasGST) / 11)) VIRTUAL,
    PRIMARY KEY (`id`),
    UNIQUE KEY `transactionItemIndex` (`id`),
    CONSTRAINT `quantityConstraint` CHECK ((`quantity` > 0)),
    CONSTRAINT `unitPrice` CHECK ((`unitPrice` > 0)),
    CONSTRAINT `unitPriceConstraint` CHECK ((`unitPrice` > 0))
) ENGINE=InnoDB AUTO_INCREMENT=5 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```
# Lab 4 and 5
### 1. Add `hasGST` boolean to track whether Item has GST
Assuming it's not already added
```sql
USE 21211711_db; /* So you don't have to repeat*/
ALTER TABLE 21211711_db.TransactionItem
ADD hasGST TINYINT(1) DEFAULT 0; /* TRUE = 1, FALSE = 0*/
```
### 2. Update Values after Insertion for a row - unitPrice and totalPrice
Assuming its already a generated column
Need to update $199.95 for Product B
```sql
UPDATE 21211711_db.TransactionItem
SET unitPrice = 199.95, totalPrice = 199.95
WHERE name = "Product B";
```
**If I wanted to update all instances where name had the word "Product" somewhere in it**
```sql
UPDATE 21211711_db.TransactionItem
SET unitPrice = 199.95, totalPrice = 199.95
WHERE name LIKE "%Product%";
```
- To match names that start with "Product": `WHERE name LIKE "Product%"`
- To match names that end with "Product": `WHERE name LIKE "%Product"`
### 3. Drop a column `totalPrice` and Generate it automatically
```sql
ALTER TABLE TransactionItem /* Step 1 Drop the totalPrice Column*/
DROP COLUMN totalPrice;

ALTER TABLE TransactionItem
ADD totalPrice FLOAT AS (unitPrice * quantity) STORED; /* Step 2 Add the totalPrice Column as a Generated Column and Store it in DB*/
```
#### Why Store the `totalPrice` as a Generated Column?
1. **Performance Optimization**: For frequently accessed or large tables, storing the generated `totalPrice` can reduce computation time, as it’s calculated only once (when `unitPrice` or `quantity` changes) rather than each time a query is executed. This is especially useful for complex calculations or when the table is used in high-frequency queries.
2. **Consistency**: Storing the generated column ensures that the `totalPrice` value is always consistent with the latest `unitPrice` and `quantity` values, as the database automatically recalculates and updates it whenever these values change.
3. **Simplified Queries**: Storing the column means you can retrieve the `totalPrice` directly without needing to calculate it in each query. This can make queries more readable and reduce the need for repetitive expressions.
4. **Indexing Possibility**: In some databases, stored generated columns can be indexed, making it faster to search or sort by `totalPrice` compared to a virtual/generated column calculated on-the-fly.
### 4. Generate column `taxAmount` 
We multiply by `hasGST` before dividing by 11 so that if GST is false = 0 then we will not calculate tax amount. Short cut easy mode.
```sql
ALTER TABLE TransactionItem
ADD `taxAmount` FLOAT GENERATED ALWAYS AS (((`totalPrice` * hasGST) / 11)) STORED;
```
### 5. Add Constraints to `unitPrice` , `quantity`, `hasGST`, `description`
**Add constraints as required below:**
a. unitPrice and quantity must be greater than zero (two constraints);
b. hasGst should be set to FALSE (0) as a default value;
c. description should not be null
```sql
ALTER TABLE TransactionItem
MODIFY unitPrice FLOAT NOT NULL,
MODIFY quantity INT NOT NULL,
ADD CONSTRAINT unitPricePositive CHECK (unitPrice > 0), /*name constraint */
ADD CONSTRAINT quantityPositive CHECK (quantity > 0),
MODIFY hasGST TINYINT(1) DEFAULT 0,
MODIFY description VARCHAR(50) NOT NULL;
```
### 6. SELECT Queries
```sql
/* Select description and unit price of items where the unit price is greater than $110.00 */
SELECT description, unitPrice
FROM TransactionItem
WHERE unitPrice > 110.00;

/* Select all columns for items that have a quantity not equal to one */
SELECT *
FROM TransactionItem
WHERE quantity <> 1;

/* Select descriptions of items where the description starts with 'B' */
SELECT description
FROM TransactionItem
WHERE description LIKE 'B%';

/* Select the description and unit price of items with unit price less than $201.00 and GST applied (hasGST = 1) */
SELECT description, unitPrice
FROM TransactionItem
WHERE unitPrice < 201.00
  AND hasGST = 1;
``` 
### 6. CREATE `Transaction` Table, FK Constraint, Populate
As per the table below, create the table `Transaction` with the below attributes and add in the values and add in Foreign Key relationship with `TransactionItem`
![Pasted image 20241030060500.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/f4328752fc3b8ce099410a84c28111c1e7beb79f.png "wikilink")
To create and populate the `Transaction` table with the provided data, and to establish a foreign key relationship with the `TransactionItem` table's `id`, follow these steps.
### Step 1: Create the `Transaction` Table

```sql
CREATE TABLE Transaction (
    id INT NOT NULL AUTO_INCREMENT,
    date DATE NOT NULL,
    customerName VARCHAR(50) NOT NULL,
    transactionItem INT NOT NULL,
    PRIMARY KEY (id),
    FOREIGN KEY (transactionItem) REFERENCES TransactionItem(id)
);
```
##### Explanation of Create 
- **id**: Auto-increment primary key for the `Transaction` table.
- **date**: Date of the transaction. The date format should match the `YYYY-MM-DD` format in MySQL.
- **customerName**: Name of the customer involved in the transaction.
- **transactionItem**: This references the `id` column in the `TransactionItem` table, establishing a foreign key relationship to ensure data consistency.
#### Step 2: Insert Data into the `Transaction` Table
Now, insert the data into the `Transaction` table with the specified dates in `YYYY-MM-DD` format.

```sql
INSERT INTO Transaction (date, customerName, transactionItem) VALUES
('2022-01-01', 'Example Corporation', 4),
('2022-01-04', 'Nikola Limited', 2),
('2023-01-04', 'Pear Computers', 1),
('2023-07-31', 'Western Mining', 3);
```
##### Explanation of Insert Statements
Each `INSERT` statement:
- **date**: The date field is formatted as `YYYY-MM-DD` to ensure compatibility with MySQL’s date format.
- **customerName**: Inserts the specified customer name.
- **transactionItem**: Specifies the `id` of the related item in the `TransactionItem` table.
### 6. Index `id` field on each `Transaction` and `TransactionItem` table
```sql
CREATE INDEX idx_transaction_id ON Transaction(id);
CREATE INDEX idx_transaction_item_id ON TransactionItem(id);
```
To create indexes on the `id` field in both the `Transaction` and `TransactionItem` tables, use the following SQL statements:

```sql
CREATE INDEX idx_transaction_id ON Transaction(id);
CREATE INDEX idx_transaction_item_id ON TransactionItem(id);
```
#### Reason for Indexing the `id` Field
`id` field is typically indexed because:
1. **Primary Key Optimization**: Since `id` is often a primary key, indexing it allows the database to quickly locate specific rows using this unique identifier.
2. **Foreign Key Relationship**: In this case, `Transaction.transactionItem` references `TransactionItem.id` as a foreign key. Indexing the `id` columns in both tables improves the performance of joins and lookups based on this foreign key relationship.
#### Advantages of Using an Index
1. **Faster Query Performance**: Indexes allow the database to find rows more quickly, significantly speeding up `SELECT`, `JOIN`, and `WHERE` operations involving the indexed `id` fields.
2. **Improved Data Integrity**: Indexes on primary keys and foreign keys enforce uniqueness and consistency, ensuring that only valid references are used and preventing duplication where it’s not allowed.
3. **Efficient Lookups in Large Tables**: Indexes improve lookup performance even as data grows, which is crucial for large datasets where sequentially scanning all rows would be too slow.
### 7 a) SELECT with Sorting `ORDER BY` `VARCHAR`
```sql
/* Select all columns from TransactionItem sorted by description from Z to A */
SELECT *
FROM TransactionItem
ORDER BY description DESC;
```
### 7 b) SELECT with Sorting `ORDER BY` by 2 Columns
```sql
/* Select all columns from TransactionItem sorted by hasGST (0, No GST first) and then by unitPrice from smallest to largest */
SELECT *
FROM TransactionItem
ORDER BY hasGST ASC, unitPrice ASC;
```
### 7 c) SELECT Sorting `ORDER BY` and `DATE` 
```sql
/* Select all columns from Transaction sorted by date from newest to oldest */
SELECT *
FROM Transaction
ORDER BY date DESC;
```
### 7 d) SELECT with Sorting `ORDER BY` 2 Columns `DATE` and `VARCHAR`
```sql
/* Select all columns from Transaction sorted by date from newest to oldest and then by customerName from Z to A */
SELECT *
FROM Transaction
ORDER BY date DESC, customerName DESC;
```
### 8 (a): SELECT Aggregation `GROUP BY`
```sql
/* Calculate the average unit price of items, grouped by their GST status */
SELECT hasGST, AVG(unitPrice) AS averageUnitPrice
FROM TransactionItem
GROUP BY hasGST;
```
### 8(b): SELECT  `GROUP BY`, `ORDER BY`, COUNT `MONTH`, `YEAR`
```sql
/* Count the number of transactions grouped by each month and year */
SELECT YEAR(date) AS year, MONTH(date) AS month, COUNT(*) AS transactionCount
FROM Transaction
GROUP BY YEAR(date), MONTH(date)
ORDER BY year, month;
```
### 8 (c): SELECT `GROUP BY` Two Columns and `AS`
```sql
/* Find the minimum total price of items, grouped by quantity and then by GST status */
SELECT quantity, hasGST, MIN(totalPrice) AS smallestTotalPrice
FROM TransactionItem
GROUP BY quantity, hasGST;
```
### 9 (d): SELECT `AS`, `WHERE` Condition and `GROUP BY`
```sql
/* Calculate the average unit price of items with unit price over $100, grouped by GST status */
SELECT hasGST, AVG(unitPrice) AS averageUnitPrice
FROM TransactionItem
WHERE unitPrice > 100
GROUP BY hasGST;
```

# Lab 6
### 1 (a): Rows that Exist in Both Tables (INNER JOIN)
```sql
/* Select rows that exist in both Transaction and TransactionItem tables */
SELECT T.*, TI.*
FROM Transaction T
INNER JOIN TransactionItem TI ON T.transactionItem = TI.id;
```
- **Explanation**: The `INNER JOIN` returns only rows where there is a match between `Transaction.transactionItem` and `TransactionItem.id`, effectively giving you rows that exist in both tables.
### 1 (b): Rows that Exist Only in the `TransactionItem` Table (LEFT JOIN with NULL check)
```sql
/* Select rows that exist only in the TransactionItem table */
SELECT TI.*
FROM TransactionItem TI
LEFT JOIN Transaction T ON T.transactionItem = TI.id
WHERE T.id IS NULL;
```
- **Explanation**: The `LEFT JOIN` returns all rows from `TransactionItem`, and any matching rows from `Transaction`. Using `WHERE T.id IS NULL` filters out rows that don’t have a match in `Transaction`, giving rows that exist only in `TransactionItem`.
### 1 (c): Rows that Exist Only in the `Transaction` Table (LEFT JOIN with NULL check)
```sql
/* Select rows that exist only in the Transaction table */
SELECT T.*
FROM Transaction T
LEFT JOIN TransactionItem TI ON T.transactionItem = TI.id
WHERE TI.id IS NULL;
```
- **Explanation**: This query uses a `LEFT JOIN` to select all rows from `Transaction`, with matching rows from `TransactionItem`. The `WHERE TI.id IS NULL` condition filters out rows that don’t have a match in `TransactionItem`, giving rows that exist only in `Transaction`.
### 2 (a): `TransactionsWithItems` – Join `Transaction` and `TransactionItem` Tables on Common Rows
```sql
/* Create the TransactionsWithItems view, joining Transaction and TransactionItem on matching rows */
CREATE VIEW TransactionsWithItems AS
SELECT T.*, TI.*
FROM Transaction T
INNER JOIN TransactionItem TI ON T.transactionItem = TI.id;

/* Verify the TransactionsWithItems view */
SELECT * FROM TransactionsWithItems;
```
### 2 (b): `GstOnlyItems` – Rows in `TransactionItem` with GST Applied
```sql
/* Create the GstOnlyItems view, selecting only rows from TransactionItem where hasGST is true */
CREATE VIEW GstOnlyItems AS
SELECT *
FROM TransactionItem
WHERE hasGST = 1;

/* Verify the GstOnlyItems view */
SELECT * FROM GstOnlyItems;
```
### 2 (c): `JanuaryTransactions` – Rows in `Transaction` Dated in January
```sql
/* Create the JanuaryTransactions view, selecting only rows from Transaction where date is in January */
CREATE VIEW JanuaryTransactions AS
SELECT *
FROM Transaction
WHERE MONTH(date) = 1;

/* Verify the JanuaryTransactions view */
SELECT * FROM JanuaryTransactions;
```
#### Explanation
Each view:
- **`TransactionsWithItems`**: Shows joined rows from `Transaction` and `TransactionItem`, so only transactions with matching items appear.
- **`GstOnlyItems`**: Filters rows in `TransactionItem` to show only items with GST applied (`hasGST = 1`).
- **`JanuaryTransactions`**: Filters rows in `Transaction` to show only transactions where the month is January (`MONTH(date) = 1`).

To create a table named `Locations` with `POINT` data type for latitude and longitude, and to insert the specified data, you can use the following SQL statements. 
### 3 GEOSPATIAL Tables Creation, Insertion
#### Step 1: Create the `Locations` Table
```sql
CREATE TABLE Locations (
    id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL,
    geometry POINT NOT NULL,
    PRIMARY KEY (id)
);
```
#### Step 2: Insert Data into the `Locations` Table
To insert the latitude and longitude as `POINT` values, use the `ST_Point` function:
```sql
INSERT INTO Locations (id, name, geometry) VALUES
(1, 'Perth', ST_Point(115.850, -31.950)),
(2, 'Joondalup', ST_Point(115.766, -31.745)),
(3, 'Mandurah', ST_Point(115.723, -32.523)),
(4, 'Armadale', ST_Point(116.015, -32.153));
```
##### Explanation
- **geometry POINT**: Stores the latitude and longitude as a spatial `POINT` data type, which is appropriate for geographic coordinates.
- **ST_Point(longitude, latitude)**: Creates a `POINT` object with the given coordinates, where the first parameter is longitude and the second is latitude.
# Lab 7
### Part 1: Alternative Visualization Suggestions
For each visualization, these are alternatives that could convey similar insights:
1. **Profit by Date as a Line Graph**  
   - **Alternative**: **Area Chart**. This could similarly show trends over time but adds emphasis to the profit volume by shading below the line.
2. **Profit by Country as a Map**
   - **Alternative**: **Choropleth Map** (filled map). Instead of points, this map shades entire countries based on profit values, which can enhance readability by making it clear which areas are performing well without hovering over points.
3. **Sales by Product and Segment as a Histogram (Bar Chart)**
   - **Alternative**: **Stacked Bar Chart**. This variant could highlight how each segment contributes to the total sales of each product, providing both individual and combined segment insights.
4. **Month and Year Slicer**
   - **Alternative**: **Timeline Slicer**. A single slider that allows users to select a date range, combining both month and year into an intuitive timeline.
5. **Text Caption for the Title**
   - **Alternative**: **Dynamic Title with Date Range Context**. Instead of a static text caption, use a dynamic title that updates based on the selected filters, such as displaying the year or date range automatically.
### Part 2: Answering Each Question with Visualizations
1. **Which month and year had the most profit?**
   - **Visualization**: Profit by Date (Line Graph)
   - **How to find the answer**: Look at the highest point on the line graph to identify the peak month and year of profit. 
2. **Where is the company seeing the most success (by country)?**
   - **Visualization**: Profit by Country (Map)
   - **How to find the answer**: Look for the country with the highest intensity (shaded area or point size) on the map. Alternatively, sort or add a tooltip to display exact values for each country.
3. **Which product and segment should the company continue to invest in?**
   - **Visualization**: Sales by Product and Segment (Bar Chart)
   - **How to find the answer**: Identify the products and segments with the tallest bars, as these represent higher sales volumes, indicating potential areas for continued investment.
### Part 3: Explanation of Symbols in Power BI’s Fields Editor
1. **Sigma (Σ)**: Indicates a numeric field that can be aggregated, such as sums or averages. 
   - **Benefit**: This helps users quickly identify which fields are suitable for calculations.
2. **Globe**: Represents a geographic field, such as country or city.
   - **Benefit**: Geographic fields can be mapped, making it easy to visualize location-based data.
3. **Calendar**: Signifies a date field.
   - **Benefit**: Date fields enable time-based analysis, allowing users to create time series visualizations like line charts and slicers.
4. **Hierarchy** (a stacked icon): Indicates fields that are part of a hierarchy, such as Year > Quarter > Month.
   - **Benefit**: Helps users drill down through data granularity, simplifying exploration from a high-level view to detailed levels.
These symbols assist users by providing quick visual cues about the data type and potential aggregation options, making data preparation and visualization setup more intuitive in Power BI.
# Lab 8
### 1. R Visuals vs Normal Visuals
- **R Visuals** require enabling and running an R script within Power BI, which can add processing time and may not be interactive like native visuals i.e. it doesn't filter other visuals because it lacks interactivity. Normal visuals are easier to set up and more responsive, designed for interactivity directly in Power BI.
### 2. Suitability of Correlation Plot for Boolean Data
- **Suitability**: Correlation plots are generally not suitable for Boolean data because correlations are typically used with continuous variables. For Boolean data, a heatmap or contingency table would be more appropriate.
### 3. Clicking Elements of the Pie Chart
- **Result**: Clicking a pie chart segment typically filters other visuals based on the selected category. This interaction helps highlight related data across different visuals for focused analysis.
### 4. Mtcars Dataset Analysis
   - **a. Correlation Between Attributes**: 
      - In correlation analysis, values range from **-1 to 1**:
         - **+1** indicates a perfect positive correlation: as one attribute increases, the other also increases proportionally.
         - **-1** indicates a perfect negative correlation: as one attribute increases, the other decreases proportionally.
         - **0** indicates no correlation: the attributes are independent of each other.
      - In the `mtcars` dataset, a positive correlation might be observed between attributes like horsepower (`hp`) and weight (`wt`), suggesting that as car weight increases, horsepower tends to increase as well, while a negative correlation might appear between `mpg` (miles per gallon) and `wt`, indicating heavier cars are less fuel-efficient.
### 5. Considerations for Colour Scale in Filled Map
- **Considerations**: Ensure the colour scale has clear contrast and intuitive progression (e.g., light to dark), aiding users in distinguishing high vs low values. It's important to accommodate colourblind-friendly options to enhance accessibility.
### 6. Filled Map vs Bubble Map
- **Filled Map**: Shades entire regions (countries/states) based on values. 
	- **Pros**: Easy for regional comparisons. 
	- **Cons**: Doesn’t show multiple data points in the same area. 
	- **Use**: Visualizing data with geographic boundaries, like population by country.
- **Bubble Map**: Places circles (bubbles) over specific points, where size represents value. 
	- **Pros**: Shows multiple data points within regions. 
	- **Cons**: Can overlap and obscure data. 
	- **Use**: Visualizing specific location-based data, like sales by city.
# Lab 9
### 1. Data Acquisition and Visualization Considerations
**a. Considerations when Acquiring Data**
   - **Source Reliability**: Ensure data comes from a reputable, unbiased source.
   - **Data Quality**: Check for completeness, accuracy, consistency, and timeliness.
   - **Relevance**: Ensure the data aligns with the objectives and scope of the analysis.
   - **Privacy and Compliance**: Make sure to follow any legal or ethical standards, particularly if the data includes sensitive information.
**b. The Importance of ‘Who’ in the Problem Statement**
   - The "who" defines the target audience or stakeholders (e.g., customers, demographic groups). This is crucial because understanding the "who" shapes the analysis, helps tailor insights, and ensures the solution is relevant and actionable for the intended users.
**c. Issues in Data Acquisition**
   - **Bias**: Data collection methods can introduce bias, leading to skewed results.
   - **Sampling Errors**: Incomplete or unrepresentative samples can mislead findings.
   - **Data Format Issues**: Inconsistent formats or missing data may require extra processing.
   - **Cost and Accessibility**: High costs or restricted access can limit available data, impacting completeness and quality.
**d. Ways to Misrepresent Data in Visualizations**
   - **Manipulating Axes**: Adjusting axis scales (e.g., omitting zero) can exaggerate differences.
   - **Cherry-Picking Data**: Selecting specific data points to support a narrative can distort reality.
   - **Inappropriate Chart Types**: Using complex or misleading chart types (e.g., 3D pie charts) can obscure data.
   - **Colour Scales and Highlighting**: Choosing colours or highlights that draw focus to certain areas can skew interpretation, especially if not proportionate to actual values.
# Lab 10
### 1. MongoDB `insertMany` and `insertOne` `_id` and `boolean` types
**`insertMany`:**
```javascript
db.createCollection("transactionsCollections")

db.transactionsCollection.insertMany([
    {
        _id: 1, // MongoDB uses `_id` instead of `id`
        description: "Item A",
        quantity: 2,
        unitPrice: 50.00,
        hasGST: true,
        totalPrice: 100.00, // Calculated as quantity * unitPrice
        taxAmount: 9.09 // Calculated as (totalPrice * hasGST) / 11
    },
    {
        _id: 2,
        description: "Item B",
        quantity: 1,
        unitPrice: 200.00,
        hasGST: false,
        totalPrice: 200.00,
        taxAmount: 0.00
    },
    {
        _id: 3,
        description: "Item C",
        quantity: 3,
        unitPrice: 30.00,
        hasGST: true,
        totalPrice: 90.00,
        taxAmount: 8.18
    },
    {
        _id: 4,
        description: "Item D",
        quantity: 5,
        unitPrice: 20.00,
        hasGST: false,
        totalPrice: 100.00,
        taxAmount: 0.00
    }
]);
```
Alternative `insertOne`
```javascript
db.createCollection("transactionsCollections")
db.transactionsCollection.insertOne({
    _id: 1, // MongoDB uses `_id` instead of `id`
    description: "Item A",
    quantity: 2,
    unitPrice: 50.00,
    hasGST: true,
    totalPrice: 100.00, // Calculated as quantity * unitPrice
    taxAmount: 9.09 // Calculated as (totalPrice * hasGST) / 11
});

db.transactions.insertOne({
    _id: 2,
    description: "Item B",
    quantity: 1,
    unitPrice: 200.00,
    hasGST: false,
    totalPrice: 200.00,
    taxAmount: 0.00
});

db.transactions.insertOne({
    _id: 3,
    description: "Item C",
    quantity: 3,
    unitPrice: 30.00,
    hasGST: true,
    totalPrice: 90.00,
    taxAmount: 8.18
});

db.transactions.insertOne({
    _id: 4,
    description: "Item D",
    quantity: 5,
    unitPrice: 20.00,
    hasGST: false,
    totalPrice: 100.00,
    taxAmount: 0.00
});

```
### 2. MongoDB Queries
#### b. Details on all items which do not have GST
```javascript
db.transactions.find({ hasGST: false });
```
This query retrieves all items where `hasGST` is `false`.
#### c. Details on all items with a quantity greater than 1
```javascript
db.transactions.find({ quantity: { $gt: 1 } });
```
This query retrieves all items where `quantity` is greater than `1`.
#### d. Details on all items except the one with an ID of 3
```javascript
db.transactions.find({ _id: { $ne: 3 } });
```
This query retrieves all items **except** the one with `_id` equal to `3`.
#### e. Details on all items with unit prices less than $100
```javascript
db.transactions.find({ unitPrice: { $lt: 100.00 } });
```
This query retrieves all items where `unitPrice` is less than `$100`. 

# Lab 11 
**Scenario 1: McClure, T. (2023). Supermarket AI meal planner app suggests recipe that would create chlorine gas**

1. **Briefly describe the situation that occurred:**
   - A supermarket's AI meal planner app suggested a recipe that could produce chlorine gas.
   - The AI combined ingredients that, when mixed, are hazardous (e.g., mixing bleach with other substances).
   - Users relying on the app could inadvertently create toxic gas at home.

2. **Briefly describe who the situation affected:**
   - Consumers using the app for meal planning.
   - The supermarket's reputation and customer trust.
   - Potentially public safety agencies if incidents occurred.

3. **Briefly describe why this situation is a problem:**
   - **Safety Risk:** Users could be exposed to harmful substances.
   - **Ethical Issue:** Negligence in ensuring AI outputs are safe.
   - **Reputational Damage:** Loss of trust in the supermarket and its technological offerings.
   - **Security Issue:** Lack of safeguards in AI to prevent dangerous recommendations.

4. **How could this problem be prevented from happening again in the future:**
   - Implement stricter safety checks and content filters in the AI system.
   - Incorporate human oversight to review AI-generated recipes.
   - Regularly update the AI's database to exclude hazardous ingredient combinations.
   - Conduct thorough testing of AI outputs before public release.

5. **Can any (non-monetary) remediation be offered:**
   - Issue a public apology and inform users about the error.
   - Update the app to correct and prevent similar issues.
   - Provide safety guidelines within the app for users.
   - Educate the development team on responsible AI practices.

---

**Scenario 2: Kost, E. (2023). How Did the Optus Data Breach Happen?**

1. **Briefly describe the situation that occurred:**
   - Optus experienced a significant data breach exposing customer information.
   - Personal data such as names, addresses, and identification numbers were compromised.
   - The breach resulted from vulnerabilities in Optus's security systems.

2. **Briefly describe who the situation affected:**
   - Millions of Optus customers whose data was exposed.
   - Optus's reputation and stakeholder trust.
   - Potential risk to other organizations due to increased cyber threats.

3. **Briefly describe why this situation is a problem:**
   - **Security Issue:** Inadequate protection of sensitive customer data.
   - **Privacy Issue:** Unauthorized access to personal information.
   - **Ethical Issue:** Failure to uphold responsibility for data security.
   - **Financial and Emotional Impact:** Customers may face fraud or identity theft.

4. **How could this problem be prevented from happening again in the future:**
   - Strengthen cybersecurity infrastructure and encryption methods.
   - Regularly conduct security audits and vulnerability assessments.
   - Implement multi-factor authentication and strict access controls.
   - Provide employee training on cybersecurity awareness.

5. **Can any (non-monetary) remediation be offered:**
   - Promptly notify affected customers and provide clear communication.
   - Offer guidance on protective measures (e.g., changing passwords).
   - Collaborate with law enforcement to address the breach.
   - Commit to transparency and improvements in data security practices.

---

**Scenario 3: Kost, E. (2023). What Caused the Medibank Data Breach?**

1. **Briefly describe the situation that occurred:**
   - Medibank suffered a cyber-attack leading to a data breach.
   - Sensitive health and personal data of customers were accessed.
   - The breach exploited security weaknesses within Medibank's systems.

2. **Briefly describe who the situation affected:**
   - Medibank customers whose confidential information was compromised.
   - The company's reputation and customer trust levels.
   - Potential impact on the broader healthcare industry's data security perception.

3. **Briefly describe why this situation is a problem:**
   - **Privacy Issue:** Exposure of sensitive health information.
   - **Security Issue:** Failure to protect against cyber threats.
   - **Ethical Issue:** Breach of confidentiality obligations.
   - **Risk of Harm:** Potential misuse of personal and health data.

4. **How could this problem be prevented from happening again in the future:**
   - Enhance cybersecurity measures, including advanced encryption.
   - Implement continuous network monitoring and threat detection.
   - Conduct regular employee training on handling sensitive data.
   - Review and update incident response plans.

5. **Can any (non-monetary) remediation be offered:**
   - Inform affected individuals and offer support services.
   - Provide resources for identity protection and credit monitoring.
   - Publicly commit to improving data security measures.
   - Engage with regulators and stakeholders to rebuild trust.

---

**Scenario 4: Warren, J. (2023). PivotNine | “Venality, Incompetence and Cowardice”**

1. **Briefly describe the situation that occurred:**
   - The article criticizes certain organizations or individuals for unethical behavior.
   - Highlights issues of corruption (venality), lack of skill (incompetence), and avoidance of responsibility (cowardice).
   - Discusses a scenario where these factors led to ethical, security, or privacy failures.

2. **Briefly describe who the situation affected:**
   - Stakeholders harmed by unethical or incompetent actions.
   - The organizations involved facing loss of credibility.
   - General public affected by the erosion of ethical standards.

3. **Briefly describe why this situation is a problem:**
   - **Ethical Issue:** Corruption undermines fairness and integrity.
   - **Security/Privacy Issue:** Incompetence can lead to data breaches or system failures.
   - **Accountability Issue:** Cowardice prevents addressing and correcting problems.
   - **Trust Erosion:** Public confidence in institutions diminishes.

4. **How could this problem be prevented from happening again in the future:**
   - Establish and enforce strict ethical guidelines and codes of conduct.
   - Ensure competent leadership through proper hiring and training practices.
   - Promote a culture of accountability and transparency within organizations.
   - Encourage whistleblowing and protect those who report unethical behavior.

5. **Can any (non-monetary) remediation be offered:**
   - Implement organizational reforms to address underlying issues.
   - Publicly acknowledge mistakes and take responsibility.
   - Engage in open dialogue with affected parties to rebuild trust.
   - Foster ethical leadership and promote best practices industry-wide.

---

**Note:** These bullet points are intended to serve as concise study notes for exam preparation on ethical, security, and privacy issues related to the provided scenarios.

#  Lab 9 Extra Content that could be relevant:
![Pasted image 20241030075959.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/6303ea2dc21ff8609512ec9f9728804efe3eb96b.png "wikilink")![Pasted image 20241030080119.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/8e77ad6e566634b21cc807e85b12cbaae7e3ff3c.png "wikilink")
![Pasted image 20241030080146.png](INMT5526%20-%20Business%20Intelligence%20Lecture%20and%20Lab%20Notes-media/4fae4a4d73c09113990d0597248c229b0cb288be.png "wikilink")
