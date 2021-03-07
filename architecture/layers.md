[Example boilerplate for Go projects](https://github.com/valonekowd/clean-architecture)

* Domain (Entity + Repository interface)
    * Encapsulate critical business rules (the most general and high-level rules) —> are the least likely to change when something external changes
    * Can be an object with methods, or a set of data structures and functions —> so long as the entities can be used by many different applications in the enterprise
    * No operational change to any particular application should affect this layer
* Use Cases / Application
    * Contains application-specific business rules
    * Orchestrate the flow of data to and from `domain` —> use `domain` business rules to achieve the goals of the use case
    * Changes to database, UI, frameworks do not affect this layer
    * Changes in this layer do not affect `domain`
* Interfaces / Adapters / Controllers / Presenters
* Infrastructures