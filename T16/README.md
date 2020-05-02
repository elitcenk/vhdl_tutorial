# T16 Use Constant And Generic Map

When define same value and type, code is useless. Constant may be used i place of signal and variables anywhere in the program. But constant value will not changed.

Constant syntax is, 

`constant <constant_name> : <type> := <value>;`

Constants can be declared along with signal.

Constants can be passed into a module through the entity by using the generic keyword. The syntax for creating an entity for a module which accepts generic constants is:

 ``` 
entity <entity_name> is
generic(
    <entity_constant_name> : <type>;
    ...
);
port(
    <entity_signal_name> : in|out|inout <type>;
    ...
);
end entity;
 ``` 

The syntax for instantiating a generic module in another VHDL file is:

 ``` 
<label> : entity <library_name>.<entity_name>(<architecture_name>)
generic map(
    <entity_constant_name> => <value_or_constant>,
    ...
)
port map(
    <entity_signal_name> => <local_signal_name>,
    ...
);
 ``` 
