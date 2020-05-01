# T12 Signed Unsigned

Signed and unsigned types in VHDL are bit vectors like `std_logic_vector`. Difference is that `std_logic_vector` useless for performing arithmetic operations.

If you add operation on `std_logic_vector`, compiler error produced. 

The syntax of signed and unsigned signal :

`signal <name> : signed(<N-bits> downto 0) := <initial_value>;`

`signal <name> : unsigned(<N-bits> downto 0) := <initial_value>;`

Initiate operation same as the `std_logic_vector`. 

In the wrapping counter example, we see that the signed and unsigned signals behave exactly the same way. Both `UnsCnt` and `SigCnt` start at 0, and are incremented one-by-one up to FF. Hex FF (decimal 255) is the largest value our 8-bit signals can hold. Therefore, the next increment wraps both of them back to 0.

We created the two 4-bit signals `Uns4` and `Sig4`, and gave them both an initial value of “1000”. We can see from the waveform that they are both just hex 8 (binary 1000).

The last two 8-bit signals we created were `Uns8` and `Sig8`. We can see from the waveform that their initial values are 0, as one would expect. But from there, they behave differently! Apparently, signed and unsigned types made a difference when adding two signals of different lengths. 
