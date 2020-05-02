# T18 Timer

In previous tutorial, we use wait for. But in the real life, we don't wait for. In real life, clock exist. Every clock tick signal changed.

To count seconds in VHDL, we can implement a counter that counts the number of clock periods which passes. When this counter reaches the value of the clock frequency, 100 million for example, we know that a second has passed and it’s time to increment another counter. Let’s call this the Seconds counter.

To count minutes, we can implement another Minutes counter which increments when 60 seconds have passed. Similarly, we can create an Hours counter for counting hours, incrementing when 60 minutes have passed.

We can continue this approach for counting days, weeks, and months too. We are limited by the available physical resources in the underlying technology as well as the length of the counter versus the clock frequency.
