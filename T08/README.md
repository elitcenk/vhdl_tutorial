# T08 If Then Elsif Else

In this tutorial, we learn if then else structure. Basic syntax is 
 ``` 
if <condition> then
elsif <condition> then
else
end if;
 ``` 
 
 elsif and else are optional. elsif can be used multiple times. <condition> can ve boolean. 
 
 Relational operators:
  - `=`	    equal
  - `/=`	not equal
  - `<`	    less than
  - `<=`	less than or equal
  - `>`	    greater than
  - `>=`	greater than or equal
 
 Logical operators:
- `not a`	    true if a is false
- `a and b`	    true if a and b are true
- `a or b`	    true if a or b are true
- `a nand b`	true if a or b is false
- `a nor b`	    true if a and b are false
- `a xor b`	    true if exactly one of a or b are true
- `a xnor b`	true if a and b are equal

In this program `countUp` and `countDown` signal exist. `countUp` signal increment and `countDown` signal decrement. Which one is bigger then print the bigger one. If there are equal print there are equal.

The output of program is

 ``` 
 VSIM 17> run
 # ** Note: CountDown is larger
 #    Time: 0 ns  Iteration: 0  Instance: /t08_iftb
 # ** Note: CountDown is larger
 #    Time: 0 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountDown is larger
 #    Time: 10 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountDown is larger
 #    Time: 20 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountDown is larger
 #    Time: 30 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: They are equal
 #    Time: 40 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 50 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 60 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 70 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 80 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 90 ns  Iteration: 1  Instance: /t08_iftb
 # ** Note: CountUp is larger
 #    Time: 100 ns  Iteration: 1  Instance: /t08_iftb
```
