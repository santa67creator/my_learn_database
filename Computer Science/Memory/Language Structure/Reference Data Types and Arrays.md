![[2026-09-06-133002_hyprshot.png]]

Array array elements can be static or dynamic depending on the language, and where they are initialized in memory will also differ. a static array is initialized on the stacks, a dynamic array is initialized on the heap.

but if you don’t go into these individual features, all elements are stored in memory sequentially to each other, so access to any element of the array is very fast

## Reference data types. Arrays
They refer to the same memory value. And changing values ​​in one variable affects another variable. *Arrays have this property.*

### ==The size of each element is 1 one byte according to the type we specified *(byte, short, int, long)*==

## **To get any array element you need to know 3 three values**
*The reference to the beginning of the array is in the variable in arr[]*
![[Pasted image 20260909062856.png]]
### EXAMPLE: We want to get 3 third element.
**The index will be 2. Two is the index of the element
Address 3 of the third element is calculated like this: 1 + 2 * 1 = 3 cell address**
1 one unit address of the beginning of the array (0x01),
*another 1 unit ==this is the size of the element in bytes== (last)*
![[Pasted image 20260909063852.png]]


# BACK PAGE --> [[Primitive Data Types]]
# NEXT PAGE --> [[Unused Memory]]