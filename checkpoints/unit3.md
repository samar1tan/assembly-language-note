# 3.1
## (1)
- 2662H
- E626H
- E626H
- 2662H
- D6E6H
- FD48H
- 2C14H
- 0000H
- 00E6H
- 0000H
- 0026H
- truncate 010CH into 000CH ~~010CH~~
## (2)
```assembly
mov ax, 6622H;  CS = 2000H, IP = 0003H, AX = 6622H
jmp 0ff0:0100;  CS = 0ff0H, IP = 0008H -> 0100H
mov ax, 2000H;  CS = 0ff0H, IP = 0103H, AX = 2000H
mov ds, ax;     CS = 0ff0H, IP = 0105H, DS = 2000H
mov ax, [0008]; CS = 0ff0H, IP = 0108H, AX = C389H
mov ax, [0002]; CS = 0ff0H, IP = 010BH, AX = EA66H
```
There is no difference between data and instruction from the perspective of memory, since they are both stored in the form of binary strings. The classification, which occurs in case of memory accessing in some relative addressing mode like CS:IP -> instruction and DS[index] -> data, is made according to their storage positions, i.e., which memory segments (code/data segment) they belong to.
# 3.2
## (1)
```assembly
mov ax, 2000H
mov ss, ax
mov sp, 10H
```
## (2)
```assembly
mov ax, 1000H
mov ss, ax
mov sp, 0
```
