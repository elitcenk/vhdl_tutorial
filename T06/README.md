# T06 Signal

In this tutorial, we learn signal which is for interact with any other logic. In the past tutorial we learn variable which only used in process. If we interact with any other logic, we must use signal.

Signal are declard between artitecture 
 
Signals are declared between the architecture <architecture_name> of <entity_name> is line and the begin statements in the VHDL file. This is called the declarative part of the architecture.

Signal syntax is `signal <name> : <type>;`
If we want initial value of signal we may use `signal <name> : <type> := <initial_value>;`


Signal and varable assignment syntax is different. A variable assign with `:=` and signal assign with `<=` . When variable assing new value, assignement executed. When signal assgn new value, not evaluated. Signal assignment executed when process waiting. Before the wait there are two assignment of signal. Bu there is one assignment. Signal variable assign the last command.


The output of program is

 ``` 
 VSIM 13> run
 # ** Note: i=0
 #    Time: 0 ns  Iteration: 0  Instance: /t05_whilelooptb
 # ** Note: i=2
 #    Time: 0 ns  Iteration: 0  Instance: /t05_whilelooptb
 # ** Note: i=4
 #    Time: 0 ns  Iteration: 0  Instance: /t05_whilelooptb
 # ** Note: i=6
 #    Time: 0 ns  Iteration: 0  Instance: /t05_whilelooptb
 # ** Note: i=8
 #    Time: 0 ns  Iteration: 0  Instance: /t05_whilelooptb
```
