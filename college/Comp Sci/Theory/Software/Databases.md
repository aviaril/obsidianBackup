[[Operating Systems]]
[[SQL]]
*database* - Organised collection of structured information, or data, typically stored electronically in a computer system. The data can then be easily accessed, managed, modified, updated, controlled and organised.

The simplest type of database is a flat tile consisting of information on a single entity.
Row = Record
Column = Field
#### Problems With Flat Tile
- Data Repetition wastes space and means more potential for data entry errors
- Data can be inconsistent if stored more than once
- The same ID number can be stored in multiple rows so you cannot retrieve a unique record with the ID 
- Multiple records may have to be deleted potentially resulting in a deletion anomaly 
- Multiple records may have to be added potentially resulting in an addition anomaly 
- Multiple records may have to be updated potentially resulting in an amendment anomaly   
##### Solving The Problems #####
*Primary Key* - A unique identifier
*Secondary key* - Does not need to be unique and is usually a field that is useful for searching.
*Foreign key* - A primary Key from another table used to link tables together.
Tables can be broken into multiple smaller tables and linked using IDs, this reduces repetition and makes the database more efficient.
secondary keys are not primary keys but instead are used for indexing and searching.
Composite/compound key - using more than one field as a primary key. 
#### Anomalies
- *Deletion anomaly* - Where data is stored multiple times one entry can be deleted but the other may not be resulting in data that should have been deleted remaining in the database
- *Addition anomaly* - Where data is stored multiple times one 

#### Normalisation####
The process of breaking a flat file down into several related tables.
- **First Normal form (1NF)** - There are no repeating fields, the data is atomic and there is a primary key.
- **Second Normal Form** (2NF) - The data is in First Normal Form and every field is dependent on the whole primary key.
- **Third Normal Form (3NF)** - The data is already in 2NF and there are no transitive relationships (non key items are dependent on each other).


For M:N relationships a link table is put in the middle to identify fields uniquely, an example of this that a doctor can have many patients and a patient can see many doctors, in this example the link table might be a table of appointments.



CSV - comma separated values is a text file with a specific format which allows data to be saved in a table. This means data can be easier to view but cannot be standardised.
JSON - Javascript Object Notation, - Stores data in human readable text that allows for fast data transfer but there are restrictions on the variety and complexity of data and it is difficult to add metadata. Syntax based on JS, Quicker to write than XML
XML - extensible markup language is a data formatting language that uses tags and attributes to define elements, the tags allow for more efficient searches for data but is generates larger files compared to other formats. cannot use arrays.