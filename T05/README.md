# T05 While Loop

In this tutorial contains whie loop. While Loop syntax is  
 ``` 
while <condition> loop
end loop; 
 ``` 
 The `<condition>` is boolean which `true` or `false`. The condition evaluated before every iteratioon of the loop. Loop will continue only if the condition is `true`.
 
Example of condition some 
 -  i is less than 15.                  `i<15`
 - i is no 11                           `i/=11`            
 - i greater than 1 and i less than 16  `i>= 1 and i<2**4`  
 
 Relation of operators
 - `=`	equal
 - `/=`	not equal
 - `<`	less than
 - `<=`	less than or equal
 - `>`	greater than
 - `>=`	greater than or equal
 
 Logical operators
 
 - `not a`	true if a is false
 - `a and b`	true if a and b are true
 - `a or b`	true if a or b are true
 - `a nand b`	true if a or b is false
 - `a nor b`	true if a and b are false
 - `a xor b`	true if exactly one of a or b are true
 - `a xnor b`	true if a and b are equal
 
 Output of program is
 
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
