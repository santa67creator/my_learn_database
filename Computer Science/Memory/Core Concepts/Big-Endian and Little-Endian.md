*There are two ways to store data in memory.*

## Big Indian - This arrangement is from left to right ->
## Little Indian - This arrangement is from right to left <-

##### The problem with both methods of storing information arises at the moment when data is transferred from one computer to another.
***For example, a message is transmitted over the Internet, the text of which is arranged in forward order, and the receiving computer stores the text in reverse order.*** 
It turns out that the message “Hello” was sent, but what comes back is this kind of bullshit.

![[Pasted image 20260902084344.png]]

#### on most computers the bytes are arranged in reverse order, from right to left

Moreover, the order is changed only by the bytes themselves, the bits inside the byte remain in the same sequence as they were.


# BACK PAGE --> [[MEMORY CORE]]
# NEXT PAGE --> [[Memory Alignment]]