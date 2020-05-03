# T22 Impure Function

An impure function can read or write any signal within its scope, also those that are not on the parameter list. We say that the function has side effects.

What we mean by side effects is that it is not guaranteed that the function will return the same value every time it is called with the same parameters. If the function can read signals that are not on the parameter list, the return value may depend on these shadow parameters as well. Also, the function may be altering external signals which are not assigned from its return value.

Although we can declare impure functions anywhere we can declare a normal, pure function, it only makes sense to use them within processes. When declared in the architecture where we normally declare our signals, none of the signals will be in its scope at compile time. Thus, an impure function cannot do anything more than a pure function can when declared in the architecture or within a package.

The motivation for using impure functions is chiefly decluttering of the code. We could manipulate any signal with a pure function simply by adding it to the parameter list, but if the parameter list becomes too long, it would obfuscate rather than simplify.

As we can see from the waveform, the module output remains unchanged after we added the impure function. We haven’t changed the logic at all, only the code.

The evaluation of the `Counter` signal has been moved from the FSM code into the new impure function `CounterExpired`. The `Counter <= 0;` line for clearing the `Counter` signal has also been moved into the impure function.

The result is a more readable FSM code which can be more easily maintained. This is subjective, but for me `CounterExpired(Seconds => 5)` is easier on the eyes than `Counter = CounterVal(Seconds => 5)`.

How far you should go with using impure functions is entirely up to you and whoever pays for your services. Some people feel that they should be used with caution because it can be harder to see through all the causes and effects of an algorithm hidden in a subprogram. Others, like me, feel that as long as you make your intentions clear, the easier to read code actually makes it less error-prone.
