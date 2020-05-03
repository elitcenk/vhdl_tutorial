# T23 Procedure In Process

Procedures that are declared in the declarative region of the architecture, cannot drive any external signals. This is simply because there are no signals in its scope at compile time. A procedure declared within a process, on the other hand, will have access to all of the signals that the process can see.

Such procedures can be used for decluttering algorithms in processes where the same operations occur several times. We could use a normal procedure where all the inputs and outputs are assigned to local signals when you call it, but that is not the point. By omitting the input and output signals from the procedure call, we must type less, and more importantly, we make the code more readable.





