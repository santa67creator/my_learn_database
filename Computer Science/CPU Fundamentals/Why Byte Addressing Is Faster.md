But despite the fact that it is multiple, it still goes to bed. The processor has to subtract 4 four memory cells at once, instead of one. Because our computers use Byte Addressing.

In fact, a byte-addressed processor will work faster than a word-addressed one due to the fact that the main type of information the processor works with is text.

We are constantly writing, reading, and editing text.
And depending on the encoding, a character can occupy a different number of bytes in memory, but the minimum size used in the ASCII standard is 7 bits

## Example
In order for us, for example, to change the second letter in the text, during byte addressing the processor needs to find the address of this character in memory and rewrite it to another character. If verbal addressing is used, then the entire string will be located in one 32-bit cell.

And in order for us to find the required character in this line, we need to place the entire cell in the register, then look bit by bit for where the desired character is, discard the extra bits, and so on. 
Thus, it turns out that for computers where work with text predominates, byte addressing is better suited. And in computers, verbal language is better suited for working with numbers.

![[Pasted image 20260930113832.png]]



# BACK PAGE --> [[REGISTERS]]
# NEXT PAGE --> [[General-Purpose Registers]]