# T03 Loop and Exit

This tutorial contains `loop` and `exit` command. Loop syntax is simple. 
 ``` 
loop
end loop;
 ```
 
 This loop continue indefinitely. Loop run until an `exit` command. The `exit` command used for break the loop. 
 
 First `Hello` printed. Then loop will start and print `Peekaboo!`. exit command break the loop and then print the `Goodbye!`.
 If we don't write the exit command loop will not stopped.
 
 Output of tutorial is
 
 ``` 
 VSIM 7>    run
 # ** Note: Hello!
 #    Time: 0 ns  Iteration: 0  Instance: /t03_looptb
 # ** Note: Peekaboo!
 #    Time: 0 ns  Iteration: 0  Instance: /t03_looptb
 # ** Note: Goodbye!
 #    Time: 0 ns  Iteration: 0  Instance: /t03_looptb
```
