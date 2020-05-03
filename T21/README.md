# T21 Function

Functions are subprograms in VHDL which can be used for implementing frequently used algorithms. A function takes zero or more input values, and it always returns a value. In addition to the return value, what sets a function apart from a procedure, is that it cannot contain Wait-statements. This means that functions always consume zero simulation time.

In VHDL, there are two types of functions, pure and impure functions. That a function is pure means that it will not be allowed to modify or read any external signal. We can be certain that when we call a pure function with certain arguments, it will always return the same value. We say that the function doesn’t have any side effects.

The syntax for declaring a function in VHDL is:
````
[pure|impure] function <function_name> (<parameter1_name> : <parameter1_type> := <default_value>;
                                        <parameter2_name> : <parameter2_type> := <default_value>;
                                        ... ) return <return_type> is
    <constant_or_variable_declaration>
begin
    <code_performed_by_the_function>
    return <value>
end function;
````
The pure/impure keyword is optional, although it will default to pure if the keyword is omitted. All parameters are treated as constants inside of the function. Thus, they cannot be changed. The default values are optional, and the function must always terminate at a return statement.

Functions have their own declarative region between the in and begin keywords. Constants, signals or variables declared here are valid only within the function itself, and they will not retain their values through subsequent calls to the function.


In the program contains function which name is `CounterVal`. This function used for calculate frequency by given minutes and seconds. Other part of program is the same as previous tutorial.
