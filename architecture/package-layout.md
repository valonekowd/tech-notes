[Reference](https://medium.com/@benbjohnson/standard-package-layout-7cdbc8391fc1)

1. Monolithic package
    * Throwing all code in a single package
    * Work very well for small applications
    * It removes any chance of circular dependencies because there are no dependencies
    * Issues
        * Extremely difficult to navigate the code
        * And isolate code
2. Rails-style layout
    * Group your code by its `functional type`
    * For example, all handlers go in `handlers` package, all controllers go in `controllers` package, and all models go in `models` package
    * Issues
        * Duplicating package’s name in type’s name (package `controller` with type `UserController`
        * Circular dependencies
3. Group by module
    * Similar to the Rails-style layout except that grouping code by `module` instead of by `function`
    * For example, may have a `users` package and an `accounts` package
    * Issues
        * Terrible naming (package `users` with model `User`)
        * Circular dependencies (`accounts.Controller` needs to interact with `users.Controller` and vice-versa)
4. A better approach
    * Rules
        * A package for domain types
            * Domain types
                * Simple data types (User, Account, Article, …)
                * Interfaces (UserService, UserUseCase, UserRepository, …) —> defines API for interacting with application
            * This makes `root package` extremely simple
            * `Root package` should not depend on any other package
        * Group sub-packages by dependency
        * Use a shared `mock` sub-package
        * Main package ties together dependencies
    * Good at
        * Isolate packages
        * Define a clear domain language across the entire application
5. Summary
    * Design domain language
    * Isolate dependencies
    * Introduce `mocks` to isolate tests
    * Tie everything together within `main` package
