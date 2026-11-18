# *Alignment* 
(memory alignment) is about **where exactly** in memory to place data so that the processor can read it **in one go**, and not in two.

Imagine the processor scooping up memory with a **fixed size spoon** - say, exactly 2 bytes at a time (if it's a 16-bit processor).

- If the data lies **exactly at the “round” address** (0, 2, 4, 6...) - the spoon scoops it up **in one clean motion**. Ready.
- If the same data lies **crossing the border** (for example, starting from address 1) - the spoon cannot pick it up at once. The processor has to:
    1. Scoop up the first piece (address 0),
    2. Discard extra bits that are not needed
    3. Scoop up the second piece (address 2),
    4. Discard the extra bits again,
    5. Glue both pieces together to get the original value.

This is **two readings instead of one** - slower, and some processor models cannot do this at all.

**Rule:** data must be placed at addresses that are multiples of its own size.

- 2-byte data → addresses 0, 2, 4, 6...
- 4-byte data → addresses 0, 4, 8, 12...
- 8-byte data → addresses 0, 8, 16, 24...

*for memory to work as efficiently as possible, words must be aligned along their natural boundaries.*

- Alignment is precisely about ensuring that the data lies exactly along the boundaries of these “words”, so that the processor’s hand can grab them in one go, and not in two.
- In the picture, “WORD” is just a caption showing: the processor reads these 2 bytes as one unit.

That's what "flattening" means - neatly laying out data along these "circular" boundaries so that memory accesses remain quick and simple, rather than spread out over two spoonfuls.

![[Pasted image 20260902092751.png]]

Look carefully at the picture itself - there is a direct clue there.

See how the cells are grouped in pairs? **0x00 and 0x01** are joined by a curly brace and signed with one word "WORD". The next pair **0x02 and 0x03** is also a “WORD”. And so on.

*the specific values of `1F` and `5E` do not make much sense on their own (this is just sample data)*
## **Processor capacity = how many bits it captures at a time, that is, the size of one “word”.**

If one word = 2 bytes, and there are 8 bits in a byte, then:

```
2 bytes × 8 bits = 16 bits
```

That’s the whole answer - since one word in the picture consists of exactly 2 bytes (and not 4 or 8), then the processor is **16-bit**.

This coincides with the text of the video itself - it directly says: _"let's take a 16-bit processor whose machine word size is 2 bytes"_. The picture is a visualization of exactly this example.

So a “word” is not some separate physical location in memory, but a **logical grouping of bytes** that depends on the architecture of a particular processor.

## **Why can't you just "take address 1":**  
The wires that lead to the processor are physically connected **only to boundaries that are multiples of the word size**. The data bus simply does not physically have wires to start reading “with a shift of one byte” - the pitchforks are where they are, they cannot be moved on the fly.

If you need data that lies “between” two such groups (for example, starting from address 1), the only way out is to **get both adjacent groups at once** (0x00-0x01 and 0x02-0x03), and then **programmatically** (through additional logic circuits) throw out the excess and glue together the necessary pieces - as we discussed earlier, these are two passes instead of one.

**Why didn’t they change it this way to make it more flexible?**  
Technically, it would be possible to add a circuit that can “shift” reading to any byte - but this:

1. Requires additional transistors and logic (the chip is more expensive and more complex),
2. Still does not remove the delay itself - shifting data by bit/byte takes time.

Therefore, manufacturers have chosen a compromise: **the bus is made hard and fast for aligned accesses**, and unaligned accesses are either emulated through double reading (slower) or completely prohibited at the architectural level (some old processors simply generated an error/crash when accessed in this way).


# BACK PAGE --> [[Big-Endian and Little-Endian]]
# NEXT PAGE --> [[Various Data Types]]