# (1) verification of mentioned theory of stack
**personal** executing results are as follows，
```assembly
mov ax, ffff
mov ds, ax

mov ax, 2200
mov ss, ax

mov sp, 0100

mov ax, [0]; ax = C0EA
add ax, [2]; ax = C0FC
mov bx, [4]; bx = 30F0
add bx, [6]; bx = 6021

push ax; sp = 00FE (push-->descending); written mem addr: 2200:0100 (dereference first), content: C0FC
push bx; sp = 00FC; written mem addr: 2200:00FE, content: 6021
pop ax; sp = 00FE; ax = 6021 (inverse push) 
pop bx; sp = 0100; bx = C0FC

push [4]; sp = 00FE; written mem addr: 2200:0100, content: 2F31
push [6]; sp = 00FC; written mem addr: 2200:01FE, content: 30F0
```
![](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/memoryLayoutC.jpg)
# (2) prologue to *interrupt* mechanism
> - We might easily find that for unknown purpose there are the value of register `CS`, `IP` and `AX` in the changed area of memory. Indeed, the value of `BP` and flag registers are also in there.
> - Why? Actually it leads to an *interrupt* when executing command `t` in `DEBUG.EXE`, and then system automatically pushes the current (of the statement executed in single-stepping) register variables into a stack so as to recover from *interrupt handler*.
