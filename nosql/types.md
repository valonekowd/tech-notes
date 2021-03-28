* Graph-oriented
  * The data models stored by graph databases are graph structures
  * A graph structure consists of nodes, edges and properties
  * Neo4j, FlockDB, OrientDB, …
* Document-oriented
  * Are designed to store data with the philosophy of storing a document
  * The data is arranged in the form of a book
    * A book can be divided into any number of chapters
    * Where each chapter can be divided into any number of topics
    * And each topic is further divided into sub-topics
    * And so on an so forth
  * Perfect option to store data that
    * Hierarchical tree-like structure
    * Does not have a fixed depth or schema
  * Have the indexes of keys stored in memory for faster searches
  * Data stored in the XML, JSON and other formats
  * Can hold scalar values, maps, lists and tuples
  * Every value stored in these datastore is always associated with a key
  * Schema-less
  * MongoDB, CouchDB, Elasticsearch …
* Column-oriented
  * Cassandra, Hadoop, HBase, …
* Key-value-oriented
  * One of the fastest and simplest NoSQL databases
  * A big hash table
  * Every value stored in the database has a key (for searching and deleting)
  * Redis, DynamoDB, …