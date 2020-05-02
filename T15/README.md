# T15 Port Map Instantiation

Modules communicate with the outside. `Port map` is the part of the module instantiation where you declare which local signals the module's inputs and outputs shall be connected to.

The syntax for an entity with a port in VHDL is:

 ``` 
entity <entity_name> is
port(
    <entity_signal_name> : in|out|inout <signal_type>;
    ...
);
end entity;
 ``` 

The syntax for instantiating such a module in another VHDL file is:

 ``` 
<label> : entity <library_name>.<entity_name>(<architecture_name>) port map(
    <entity_signal_name> => <local_signal_name>,
    ...
);
 ``` 
The `<label>` can be any name, and it will show up in the hierarchy window in ModelSim. The `<library_name>` for a module is set in the simulator, not in the VHDL code. By default every module is compiled into the work library. The `<entity_name>` and `<architecture_name>` must match the module we are creating an instance of. Finally, each of the entity signals must be mapped to a local signal name.


We named the architecture of the testbench sim, for simulation. The architecture of the design module was named rtl, which stands for register-transfer level. These are just naming conventions. When you see a file with such a name, you immediately know whether it’s a testbench or a design module. Different companies may have different naming conventions.
