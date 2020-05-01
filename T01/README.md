# T01 Hello World

VHDL file contains some object.

- Firstly, describe entity which name is T01_HelloWorldTb. Entity, does not input and outpur.
- Secondly, contains architecture. Which contains process.
- Thirdly, process is print the output of Hello World. Process end with wait command which break the process. If we don't write the wait command, process is never end. It will loop infinite loop. 


Output of program is

 ``` 
VSIM 2> run
# ** Note: Hello World!
#    Time: 0 ns  Iteration: 0  Instance: /t01_helloworld
```
