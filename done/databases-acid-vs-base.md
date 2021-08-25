# Graph Databases for Beginners: ACID vs. BASE Explained

## ACID
- Atomic: Everything or nothing

- Consistent: on the completion of a transaction, the database is structurally health

- Isolated: transactions do not contend with one another. Controversial access to data is moderated by database

- Durable: the results of applying transaction are permanent


This properties mean that when a **transaction succeded** the data is **CONSISTENT** and **STABLE** on dist


## BASE
More optimistic and less worried about data safety.
Data will be consistent in the future.
Primarily used by aggregate stores, including column family, key-value and document stores

- Basic Availability: database works most of the time

- Soft State: stores  dont have to be write-consistent

- Eventual conssitency: stores is consistet at some later point (maybe at read time)


## Conclusion

BASE can scale so much better than ACID in term of performance and volume, but you will have much less data guarantees, you should know how to deal with this.

BASE is low coupled to structure/data model changes



https://neo4j.com/blog/acid-vs-base-consistency-models-explained/
https://www.upwork.com/resources/nosql-vs-sql
