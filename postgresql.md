# POSTGRESQL

### That Postgres Index Types you know?
- B-Tree - index creates a tree that will keep itself balanced and even.
B-tree indexes are valuable on the most common data types such as text, numbers, and timestamps.

- Generalized Inverted Indexes, commonly referred to as GIN, are most useful when you have data types that contain multiple values in a single column.

The most common data types that fall into this bucket are:
-  hStore
- Arrays
- Range types
- JSONB

- GiST indexes are most useful when you have data that can in some way overlap with the value of that same column but from another row. 

The most common datatypes where you want to leverage GiST indexes are
- Geometry types
- Text when dealing with full-text search

GiST indexes have some more fixed constraints around size, whereas GIN indexes can become quite large.

-Block range indexes (BRIN) - best when there is some natural ordering to the data, and the data tends to be very large.
When you have very large datasets that are ordered such as dates or zip codes BRIN indexes allow you to skip or exclude a lot of the unnecessary data very quickly. BRIN additionally are maintained as smaller indexes relative to the overall datasize making them a big win for when you have a large dataset.

- Hash indexes have been around for years within Postgres, but until Postgres 10 came with a giant warning that they were not WAL-logged. 
Hash indexes at times can provide faster lookups than B-Tree indexes, and can boast faster creation times as well. The big issue with them is they’re limited to only equality operators so you need to be looking for exact matches. This makes hash indexes far less flexible than the more commonly used B-Tree indexes and something you won’t want to consider as a drop-in replacement but rather a special case.

### How work in Sql - Operator Vacuum?
VACUUM reclaims storage occupied by dead tuples. In normal PostgreSQL operation, tuples that are deleted or obsoleted by an update are not physically removed from their table; they remain present until a VACUUM is done. Therefore it's necessary to do VACUUM periodically, especially on frequently-updated tables.
 