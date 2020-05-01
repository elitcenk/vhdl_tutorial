# T13 Concurent Statement

A concurrent statement in VHDL is a signal assignment within the architecture, but outside of a normal process construct. The concurrent statement is also referred to as a concurrent assignment or concurrent process.
 
 When you create a concurrent statement, you are actually creating a process with certain, clearly defined characteristics. Concurrent statements are always equivalent to a process using a sensitivity list, where all the signals to the right of the signal assignment operator are on the sensitivity list.
 
 These shorthand notation processes are useful when you want to create simple logic which results in the assignment of a single signal. Instead of typing out a full process construct with sensitivity lists and all of that, you can simply assign to the target signal directly in the architecture.
