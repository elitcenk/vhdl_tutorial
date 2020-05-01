# T14 Case When Statement
Case When statement like if then else statement. 

Other programming languages have similar constructs, using keywords such as a switch, case, or select. Among other things, Case-When statements are commonly used for implementing multiplexers in VHDL. Continue reading, or watch the video to find out how!

The basic syntax for the Case-When statement is:
 ``` 
case <expression> is
    when <choice> =>
        code for this branch
    when <choice> =>
        code for this branch
    ...
end case;
 ``` 

The `<expression>` is usually a variable or a signal. The Case statement may contain multiple when choices, but only one choice will be selected.

The `<choice>` may be a unique value like "11":

`when "11" =>`

Or it can be a range like `5 to 10`:

`when 5 to 10 =>`

It can contain several values like `1|3|5`:

`when 1|3|5 =>`

And most importantly, the `others` choice. It is selected whenever no other choice was matched:

`when others =>`

The `others` choice is equivalent to the `Else` branch in the If-Then-Elsif-Else statement.

Output of the program is 

 ``` 
VSIM 2> run
# ** Warning: NUMERIC_STD."=": metavalue detected, returning FALSE
#    Time: 50 ns  Iteration: 1  Instance: /t14_casewhentb
# ** Warning: NUMERIC_STD."=": metavalue detected, returning FALSE
#    Time: 50 ns  Iteration: 1  Instance: /t14_casewhentb
# ** Warning: NUMERIC_STD."=": metavalue detected, returning FALSE
#    Time: 50 ns  Iteration: 1  Instance: /t14_casewhentb
# ** Warning: NUMERIC_STD."=": metavalue detected, returning FALSE
#    Time: 50 ns  Iteration: 1  Instance: /t14_casewhentb
 ``` 
