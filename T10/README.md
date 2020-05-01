# T09 std_logic
The most common type used in VHDL is the `std_logic`. Think of this type as a single bit, the digital information carried by a single physical wire. The `std_logic` gives us a more fine-grained control over the resources in our design than the `integer` type, which we have been using in the previous tutorials.

Normally, we want a wire in a digital interface to have either the value `1` or `0`. These two values are the only values that a bit, a binary digit, can have. But in reality, a physical digital signal can be in a number of states, which the std_logic type does a good job emulating. Therefore it is the most frequently used type in VHDL.

The `std_logic` type can have the following values:

- `1`	Logic 1
- `0`	Logic 0
- `Z`	High impedance
- `W`	Weak signal, can’t tell if 0 or 1
- `L`	Weak 0, pulldown
- `H`	Weak 1, pullup
- `-`   Don’t care
- `U`	Uninitialized
- `X`    Unknown, multiple drivers

This may seem like a lot of different states for a type that is supposed to model a single binary value. Don’t worry, we won’t be using all these types in this tutorial series. We will be using `1` and `0` of course. And we will also be seeing `U` and `X`, which will help us spot errors in our design. The other values are advanced VHDL features which can be used for things like modeling communication with for example I2C devices, or for creating tri-state buses.

If several processes are trying to write different values to a signal, we say that it has multiple drivers. If a std_logic signal has multiple drivers, it won’t be a compilation or run-time error, at least not in the simulator. That is because `std_logic` is a resolved type, meaning that its value will be determined by a resolution function.


The output of program is

 ``` 
 VSIM 2> run
 # ** Note: Process A: Jackpot
 #    Time: 40 ns  Iteration: 1  Instance: /t09_sensitivitylisttb
 # ** Note: Process B: Jackpot
 #    Time: 40 ns  Iteration: 1  Instance: /t09_sensitivitylisttb
```
