* `To understand the CPU or memory utilization` within a program in order `to optimize for execution time, size, or reliability`
  * After a profile of a computer program is taken with a `profiler`, a `report` is created
  * This report, often called a `profile`, can tell you information about the program that you ran

* CPU profiling reasons
  * Check performance improvements in new releases of software
  * Validate how much CPU is being utilized for each task
  * Limit CPU utilization in order to save money
  * Understanding where latency comes from
  
* Memory profiling reasons
  * Incorrect usage of global variables
  * Goroutines that don't complete
  * Incorrect reflection usage
  * Large string allocation

* We can implement profiling in many stages of Go software development
  * Development (engineering), the creation of new functions (features)
  * Testing
  * Production

* It is important to remember
  * As more metrics are being collected on a continuous basis in your running binaries —> add a small performance penalty
  * But adding an additional (e.g: 5%) overhead for CPU and memory profiling is worth the cost in order to consistently write performant code —> this trade-off is acceptable