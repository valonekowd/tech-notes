* `RE`mote `DI`ctionary `S`erver -> `REDIS`
* `In-memory` data structure storage
* `Key-value` store
* Offers persistence
* Commands for each data type for common access patterns, with bulk operations
* Support partial transaction
* Pub/Sub
* Stream
* Master/Slave replication
* Typically used in
    * `Caching`
        * A general purpose cache
        * Keys are strings
        * Values are strings, lists, hashes, sets, sorted sets, …
        * Common operations: SET and GET
    * `Message broker`
        * Message queues
        * Pub/Sub
        * Streams
    * `Database` (not recommended)
* Use cases
    * Session store
    * Rate limiting
    * Job & Queue
    * Leaderboard