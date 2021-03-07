* Independent of frameworks
    * The architecture does not depend not the existence of some libraries
    * This allows you to use such frameworks as tools, rather than forcing you to cram your system into their limited constraints
* Testable
    * The business rules can  be  tested without the UI, database, web server or any other external element
* Independent of the UI
    * The ui can change easily without changing the rest of the system
    * A web UI could be replaced with a console UI without changing the business rules
* Independent of the database
    * You  can swap out Oracle or SQL Server for Mongo, COuchDB, …
    * Your business rules are not bound to the database
* Independent of any external agency
    * In fact, your business rules don’t know anything at all about the interfaces to the outside world