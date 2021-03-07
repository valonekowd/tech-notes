* Benefits
    * Reduce the round trip time (RTT)
    * Reduce context switching both in the client and server —> when the server or client need to read from/write to the network, a sys-call is made and an expensive context switch happens between user space and kernel space. If we send 10 messages, each with  a single command, 10 context switches  will happens. If we send a single message with 10 commands, it’s likely that a single context switch will be needed
    * A huge amount of operations can be performed per second in a given Redis server
* Drawbacks
    * Not atomic (between pipelines)
    * Only get all responses in the end (when all commands done)
        * 3 commands A (1s), B (2s), C (3s)
        * So we must wait at least 3s to get A’s response
        * It is not efficiently if A’s response is the input for a subsequent command (D)
        * Then D will be blocked —> bad
* Used when
    * need performance
    * Have  several commands to send to the Redis server
    * Do not need the response of a previous command as input for a subsequent command
