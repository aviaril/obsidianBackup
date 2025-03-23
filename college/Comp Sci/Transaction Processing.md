## ACID
### Atomicity 
- transactions follow an 'All or nothing' rule 
	- if one part of the transaction fails all of the transaction will fail so no change is made 
- e.g. is a bank payment fails after taking money from one account but before paying another the entire transaction is cancelled instead of the money being burnt 
### Consistency 
- If a transaction does not conform to the databases rules the entire transaction will be rolled back 
- 
### Isolation 
- Multiple transactions happening at the same time do not conflict with each other 
- utilises record locking, when the transaction starts it will lock records that it is accessing so that only one transaction can access them at a time 
### Durability 
- Any transaction committed to the database will not be lost 
- done through backups and transaction logs 
