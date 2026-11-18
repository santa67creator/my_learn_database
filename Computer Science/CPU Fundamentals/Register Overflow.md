## what will happen to the register if we try to write a number into it that does not fit into its dimensions?
For example, we have 8-bit registers and we add two numbers 120 plus 10.
Both numbers 120 and 10 fit into one byte, so first we will write them into the AH and AL registers. **(MOV AH, 120) (MOV AL, 10)**
And now we will try to add them, writing the result to the AH register. **(ADD AH, AL)**
![[Pasted image 20261009113825.png]]
The problem here is that the sign byte contains numbers from minus 128 to 127. That is, the result of the expression 130 simply will not fit into this register, in this case the so-called ==overflow== occurs

---

## overflow can occur in two cases 
if two large positive numbers are added, or two large negative numbers are subtracted. 
in this case, the most significant bits that do not fit into the register are cut off and the result will be the number that remains after this cut-off
![[Pasted image 20261009114216.png]]

---
actually overflow means that after going abroad
permissible, we continue counting from the opposite end.
*(127 + 7 + 3)*, 
in this example we reach 127 and all that remains is to add three more 
*(120 + 7 = 127)*
adding one we get to the opposite end. to the number minus 128. *(127 + 1 = -128)* 
and continue to add to it.
*(-128 + 2 = -126)*
so the output is minus 126
![[Pasted image 20261009115033.png]]

==if we add a number with one sign, the output gets another sign, then an overflow has occurred==

#FULL SCHEME
![[Pasted image 20261009115800.png]]


# BACK PAGE --> [[Special-Purpose Registers]]
# NEXT PAGE --> [[Opcodes]]