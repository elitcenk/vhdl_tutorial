# T07 Wait On Wain Until

In this tutorial, we learn `wait on` and `wait until`. `Wait on` statement will pause the process until one of the signals change.

`wait on <signal_name1>, <signal_name2> ...;`

`Wait until` statement will pause until an condition to become true.

`wait until <condition>;`

In fact, Wait On, Wait Until and Wait For can be combined:

`wait on <signal_name1> until <condition> for <time_value>;`

This example will pause for 10 nanoseconds, or until signal1 changes and signal2 is equal to signal3:

`wait on signal1 until signal2 = signal3 for 10 ns;`

In this program first process, one signal increment and one signal decrement. Second process, wait on some changed on signals. Third process, wait until two signal are equal.
The output of program is

 ``` 
 VSIM 2> run
 # ** Note: CountUp=1 CountDown=9
 #    Time: 0 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=2 CountDown=8
 #    Time: 10 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=3 CountDown=7
 #    Time: 20 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=4 CountDown=6
 #    Time: 30 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=5 CountDown=5
 #    Time: 40 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: Jackpot!
 #    Time: 40 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=6 CountDown=4
 #    Time: 50 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=7 CountDown=3
 #    Time: 60 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=8 CountDown=2
 #    Time: 70 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=9 CountDown=1
 #    Time: 80 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=10 CountDown=0
 #    Time: 90 ns  Iteration: 1  Instance: /t07_waitonuntiltb
 # ** Note: CountUp=11 CountDown=-1
 #    Time: 100 ns  Iteration: 1  Instance: /t07_waitonuntiltb
```
