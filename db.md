# Database Theory

### Describe diffrent indexes in db that you know?

Первичный индекс (primary index)
Первичный индекс содержит поля с ключами таблицы и указатель на неключевые поля таблицы. Первичный индекс создается автоматически при создании таблицы в базе данных.

Вторичный индекс (secondary index)
Он используется для индексации полей, которые не являются ни полями упорядочения, ни ключевыми полями (нет гарантии, что файл организован по ключевому полю или первичному ключевому полю). Одна запись индекса для каждого кортежа в файле данных (плотный индекс) содержит значение индексированного атрибута и указатель на блок/запись.

Плотный индекс (dense index)
Плотный индекс в базах данных - это файл с парами ключей и указателей для каждой записи в файле данных. Каждый ключ в этом файле связан с определенным указателем на запись в файле отсортированных данных. В кластерных индексах с дублирующимися ключами плотный индекс указывает на первую запись с этим ключом.

Разреженный индекс (sparse index)
Разреженный индекс в базах данных - это файл с парами ключей и указателей для каждого блока в файле данных. Каждый ключ в этом файле связан с определенным указателем на блок в файле отсортированных данных. В кластерных индексах с дублирующимися ключами разреженный индекс указывает на самый низкий поисковый ключ в каждом блоке.

### What is Transaction?
Транзакция является рабочей единицей работы с базой данных (далее – БД). 
Это последовательность операций, выполняемых в логическом порядке пользователем, либо программой, которая работает с БД.

Мы можем сказать, что транзакция – это распространение изменений в БД. 
Например, если мы создаём, изменяем или удаляем запись, то мы выполняем транзакцию. 
Крайне важно контролировать транзакции для гарантирования.

### Describe what ACID?
Основные концепции транзакции описываются аббревиатурой ACID – Atomicity, Consistency, Isolation, Durability (Атомарность, Согласованность, Изолированность, Долговечность).

Атомарность

Атомарность гарантирует, что любая транзакция будет зафиксирована только целиком (полностью). Если одна из операций в последовательности не будет выполнена, то вся транзакция будет отменена. Тут вводится понятие “отката” (rollback). Т.е. внутри последовательности будут происходить определённые изменения, но по итогу все они будут отменены (“откачены”) и по итогу пользователь не увидит никаких изменений.

Согласованность

Это означает, что любая завершённая транзакция (транзакция, которая достигла завершения транзакции – end of transaction) фиксирует только допустимые результаты. Например, при переводе денег с одного счёта на другой, в случае, если деньги ушли с одного счёта, они должны прийти на другой (это и есть согласованность системы). Списание и зачисление  – это две разные транзакции, поэтому первая транзакция пройдёт без ошибок, а второй просто не будет. Именно поэтому крайне важно учитывать это свойство и поддерживать баланс системы.

Изолированность

Каждая транзакция должна быть изолирована от других, т.е. её результат не должен зависеть от выполнения других параллельных транзакций. На практике, изолированность крайне труднодостижимая вещь, поэтому здесь вводится понятие “уровни изолированности” (транзакция изолируется не полностью).


### What is DB Normalization?
Database Normalization is a technique of organizing the data in the database. Normalization is a systematic approach of decomposing tables to eliminate data redundancy(repetition) and undesirable characteristics like Insertion, Update and Deletion Anamolies. It is a multi-step process that puts data into tabular form, removing duplicated data from the relation tables. Following Noramlization Rules.

### What is DB DeNormalization?
Denormalization is a strategy used on a previously-normalized database to increase performance. In computing, denormalization is the process of trying to improve the read performance of a database, at the expense of losing some write performance, by adding redundant copies of data or by grouping data.
This can help us avoid costly joins in a relational database. Note that denormalization does not mean not doing normalization. It is an optimization technique that is applied after doing normalization.

It is often motivated by performance or scalability in relational database software needing to carry out very large numbers of read operations. Denormalization differs from the unnormalized form in that denormalization benefits can only be fully realized on a data model that is otherwise normalized.

For example, in a normalized database, we might have a Courses table and a Teachers table.Each entry in Courses would store the teacherID for a Course but not the teacherName. When we need to retrieve a list of all Courses with the Teacher name, we would do a join between these two tables.
In some ways, this is great; if a teacher changes is or her name, we only have to update the name in one place.
The drawback is that if tables are large, we may spend an unnecessarily long time doing joins on tables.
Denormalization, then, strikes a different compromise. Under denormalization, we decide that we’re okay with some redundancy and some extra effort to update the database in order to get the efficiency advantages of fewer joins.

Pros of Denormalization:-

Retrieving data is faster since we do fewer joins
Queries to retrieve can be simpler(and therefore less likely to have bugs),
since we need to look at fewer tables.
Cons of Denormalization:-

Updates and inserts are more expensive.
Denormalization can make update and insert code harder to write.
Data may be inconsistent . Which is the “correct” value for a piece of data?
Data redundancy necessitates more storage.

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

### MYSQL: the main differences between INNODB and MYISAM storage engine.
The main difference between MyISAM and INNODB are :

- MyISAM does not support transactions by tables while InnoDB supports.
- There are no possibility of row-level locking, relational integrity in MyISAM but with InnoDB this is possible.
- MyISAM has table-level locking.
- InnoDB does not support FULLTEXT index while MyISAM supports.
- Performance speed of MyISAM table is much higher as compared with tables in InnoDB.
- InnoDB is better option while you are dealing with larger database because it supports transactions, volume while 
- MyISAM is suitable for small project.
- As InnoDB supports row-level locking which means inserting and updating is much faster as compared with MyISAM.
- InnoDB supports ACID (Atomicity, Consistency, Isolation and Durability) property while MyISAM does not support.
- In InnoDB table,AUTO_INCREMENT field is a part of index.
Once table in InnoDB is deleted then it can not re-establish.
- InnoDB does not save data as table level so while implementation of select count(*) from table will again scan the whole table to calculate the number of rows while MyISAM save data as table level so you can easily read out the saved row number.
- MyISAM does not support FOREIGN-KEY referential-integrity constraints while InnoDB supports.