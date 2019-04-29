# Database Theory

### What is DB Normalization?
Database Normalization is a technique of organizing the data in the database. Normalization is a systematic approach of decomposing tables to eliminate data redundancy(repetition) and undesirable characteristics like Insertion, Update and Deletion Anamolies. It is a multi-step process that puts data into tabular form, removing duplicated data from the relation tables. Following Noramlization Rules.

###  Normalization Rules
Normalization rules are divided into the following normal forms:

- First Normal Form
- Second Normal Form
- Third Normal Form
- BCNF
- Fourth Normal Form

- First Normal Form (1NF)
For a table to be in the First Normal Form, it should follow the following 4 rules:
It should only have single(atomic) valued attributes/columns.
Values stored in a column should be of the same domain
All the columns in a table should have unique names.
And the order in which data is stored, does not matter.

- Second Normal Form (2NF)
It should be in the First Normal form.
And, it should not have Partial Dependency.

- Third Normal Form (3NF)
It is in the Second Normal form.
And, it doesn't have Transitive Dependency.


### Do you now that is replication?
Database replication is a technique through which an instance of a database is exactly copied to, transferred to or integrated with another location. Database replication enables the copying of a database file from a master database management system (DBMS) and its exact deployment on a slave DBMS.
Types of Data Replication:

- Transactional Replication – In Transactional replication users receive full initial copies of the database and then receive updates as data changes. Data is copied in real time from the publisher to the receiving database(subscriber) in the same order as they occur with the publisher therefore in this type of replication, transactional consistency is guaranteed. Transactional replication is typically used in server-to-server environments. It does not simply copy the data changes, but rather consistently and accurately replicates each change.
- Snapshot Replication – Snapshot replication distributes data exactly as it appears at a specific moment in time does not monitor for updates to the data. The entire snapshot is generated and sent to Users. Snapshot replication is generally used when data changes are infrequent. It is bit slower than transactional because on each attempt it moves multiple records from one end to the other end. Snapshot replication is a good way to perform initial synchronization between the publisher and the subscriber.
- Merge Replication – Data from two or more databases is combined into a single database. Merge replication is the most complex type of replication because it allows both publisher and subscriber to independently make changes to the database. Merge replication is typically used in server-to-client environments. It allows changes to be sent from one publisher to multiple subscribers.

### NoSQL or SQL: which one is better? Why?
SQL DB has:
- one language SQL
- requires that you use predefined schemas
- vertically scalable
- table-based
- better option for applications that require multi-row transactions - such as an accounting system - or for legacy systems that were built for a relational structure

Conclusion:
good choice for businesses that have rapid growth or databases with no clear schema definitions

NoSQL databases has
- defferent syntax
-  dynamic schema
- horizontally scalable
- Flexibility
- Have different types: column-oriented, document-oriented, graph-based or organized as a KeyValue

Conclusion:
will benefit from its pre-defined structure and set schemas

### What is Aggregation function in Db theory?

An aggregate function performs a calculation one or more values and returns a single value.
For example in SQL.
The aggregate function is often used with the GROUP BY clause and HAVING clause of the SELECT statement.