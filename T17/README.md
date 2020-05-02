# T17 Clocked Process

Flip flop, copies from the input to the output when the clock signal arrives. Output held, when new clock signal arrives.

Array oy flip flop called register. When clock triggered, all flip flop output changed and last output hold the value. The clock signal effectively creates timesteps in the data flow. 

This is a template for creating a clocked process with synchronous reset:

 ``` 
process(Clk) is
begin
    if rising_edge(Clk) then
        if nRst = '0' then
            <reset all output signals here>
        else
            <main logic here>
        end if;
    end if;
end process;
 ``` 

When clock rising true, output is inputted. Reset input, flip flop output to 0. 
