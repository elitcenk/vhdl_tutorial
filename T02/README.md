# T02 Wait For

This tutorial show wait for statement. Wait statement do the process stop. Wait For statement do the wait for some time.

The syntax of the wait for statement is: `wait for <time_value> <time_unit>;` 

<time_value> is number and <time_unit> is some type of time.

- fs	->  femtoseconds
- ps	->  picoseconds
- ns	->  nanoseconds
- us	->  microseconds
- ms	->  milliseconds
- sec	->  seconds
- min	->  minutes
- hr	->  hours
 
 ``` 
VSIM 5> run
# ** Note: Peekaboo!
#    Time: 0 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 10 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 20 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 30 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 40 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 50 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 60 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 70 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 80 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 90 ns  Iteration: 0  Instance: /t02_waitfortb
# ** Note: Peekaboo!
#    Time: 100 ns  Iteration: 0  Instance: /t02_waitfortb
```
