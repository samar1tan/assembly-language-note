# Convertion (also applies to all other units)
- The following answers are made without the guarantee of correctness and integrity.  
- These answers are numbered by the standalone serial numbers of corresponding checkpoints (NOT sections) in the textbook. 
# 2.1
## (2)
```assembly
mov ax, 2
add ax, ax
add ax, ax
add ax, ax
```
# 2.2
## (1)
- 0010H
- 0010H + FFFFH = 1000FH ~~0010H + FFFFH - 1 = 1000EH~~
## (2)
- round `(20000H - FFFFH) / 16` towards +inf = 1001H ~~(20000H - FFFFH) / 16 = 1000H~~
- 20000H / 16 = 2000H
# 2.3
4 times:
1. after `mov` being read
2. after `sub` being read
3. after `jmp` being read
4. after `jmp` being executed



The final value of IP is 0
