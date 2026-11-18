# Different types of data - ***they all define their content and amount of space, 
which will be allocated in memory***
![[Pasted image 20260905135354.png]]


![[Pasted image 20260905142139.png]]
*the int type takes up 32 bits in memory, and if we put the number 7 there, for which 1 byte would be enough, then 32 bits will still be allocated in memory, because the int type clearly indicates this.*
The seven will be written to the low-order bits, and the high-order bits will be filled with zeros.

## A number can be either positive or negative, and the way such numbers are stored in memory will vary greatly. 

![[Pasted image 20260905142706.png]]
*Positive numbers, also known as unsigned numbers, are perceived as they are.* 
For example, a byte completely filled with units when converted to decimal form will give the number 255. ==Therefore, it turns out that the unsigned byte type can store a number from 0 to 255.== 

# But if signed types are used signed 
then the numbers that can be written in byte *will be in the range from minus 128 to 127, and therefore ==such a number will no longer be 255 but something else==*
![[Pasted image 20260905143052.png]]

## we cannot store the minus sign in memory, so we need a special form of storage so that the processor can continue to work with this number
this formula is called [[Storing Negative Integers (Two’s Complement)]]


# BACK PAGE --> [[Memory Alignment]]

# NEXT PAGE --> [[Storing Negative Integers (Two’s Complement)]]