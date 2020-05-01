# T09 Sensitive List

In the wait on and wait until tutorial we learn them. In this tutorial we learn sensitive list. When there are some changes on signal process are triggered.

The syntax for a process with a sensitivity list is:

 ```
process(<signal1>, <signal2>, ..) is
begin
    <main logic here>
end process;
 ```
When there are some changed on signal process triggered.

The output of program is

 ``` 
 VSIM 2> run
 # ** Note: Process A: Jackpot
 #    Time: 40 ns  Iteration: 1  Instance: /t09_sensitivitylisttb
 # ** Note: Process B: Jackpot
 #    Time: 40 ns  Iteration: 1  Instance: /t09_sensitivitylisttb
```
