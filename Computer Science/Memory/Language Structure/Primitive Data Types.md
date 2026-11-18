numeric types (int, byte and similar) are **primitive types**, and their main feature is that they are **copied by value**.

![[Pasted image 20260906131007.png]]

Imagine: you have a variable `x = 5`. A cell is allocated in memory for it, and the number 5 is there.

Now you do `y = x`. What's happening:

- The computer **doesn't** say "let `y` look in the same direction as `x`".
- Instead, it takes the value from cell `x` (that is, 5), **creates a new separate memory location** and copies the same value there.

You end up with **two different lockers with the same contents** rather than one locker with two tags. `x` and `y` are completely independent variables.

Therefore, if after this you do `x = 10`, the value of `y` will not change in any way - it will remain 5, because it lives in its own cell.

## Why is this important to understand? 
Because it's the exact opposite of **reference types** (like arrays)
It's the other way around: Both names point to the same locker, and changes through one variable are also visible through the other. 
*not the data itself is copied, but only the **address** (link) to it.*


# BACK PAGE --> [[Language Structure]]

# NEXT PAGE --> [[Reference Data Types and Arrays]]