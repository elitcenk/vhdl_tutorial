# T20 Finite State Machine

A finite-state machine (FSM) is a mechanism whose output is dependent not only on the current state of the input, but also on past input and output values.

State-machines in VHDL are clocked processes whose outputs are controlled by the value of a state signal. The state signal serves as an internal memory of what happened in the previous iteration.

Once we have our enumerated type, we can declare a signal of the new type which can be used for keeping track of the FSM’s current state.
````
The syntax for declaring a signal with an enumerated type in VHDL is:
type <type_name> is (<state_name1>, <state_name2>, ...);
signal <signal_name> : <type_name>;
````

Template for one-process state machine:
````
process(Clk) is
begin
    if rising_edge(Clk) then
        if nRst = '0' then
            State <= <reset_state>;
        else
            case State is
                when <state_name> =>
                    <set_outputs_for_this_state_here>
                    if <state_change_condition_is_true> then
                        State <= <next_state_name>;
                    end if;
                ...
            end case;
        end if;
    end if;
end process;
````

In this program declared traffic light state. Then in case operation state evaluated. What state is occured then related light opened. Counter used for what time for open light. State occured then next state selected.
