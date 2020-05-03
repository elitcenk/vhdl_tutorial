# T19 Procedure

Procedure is like a function. When you down write repeated code you can write a procedure. 

Procedure may be declared within any declarative region. The scope of procedure is declared architecture, package, process. Procedure doesn't return a value. But you can return value by `out` or `inout` signals in the parameter list.

The basic syntax for creating a procedure is:

````
procedure <procedure_name> (signal|variable|constant <name1> : in|out|inout <type>;
                            signal|variable|constant <name2> : in|out|inout <type>;
                            ... ) is
    <declarations_for_use_within_the_procedure>
begin
    <code_performed_by_the_procedure_here>
end procedure;
````

A procedure’s parameter list defines its inputs and outputs, kind of like a mini-module. It can be a signal or a constant, but unlike a module, it can also be a variable. You can declare objects between the “is” and “begin” keywords that are only valid inside the procedure. These may include constants, variables, types, subtypes, and aliases, but not signals.

The first item on the parameter list for the `IncrementWrap` procedure is the `Counter` signal. It’s declared using direction `inout` for the procedure to be able to both read and set its value.

The second and third items on the parameter list are constants. This means that the values you put in here will appear as constants inside of the procedure. The `WrapValue` input together with the Enable input determines if the `Counter` signal is incremented or wrapped.

The last item on the parameter list is a variable with direction `out`. The purpose of this output is to inform the caller of the procedure that the counter wrapped. We use it here kind of like a return value.

In the main process we have four calls to the `IncrementWrap` procedure. Each of the subsequent calls use the Wrap variable to enable the counting. It wouldn’t have worked if we had used a signal instead of a variable, because signal values are only updated when a process goes to sleep. We need the output value from one procedure call to be be used as an input to a call on the very next line. Thus, it has to be a variable.
