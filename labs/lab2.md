# (1) check-off for mentioned theory of stack
executing results are as follows，
```assembly
mov ax, ffff
mov ds, ax

mov ax, 2200
mov ss, ax

mov sp, 0100

mov ax, [0]; ax = 
add ax, [2]; ax = 
mov bx, [4]; bx = 
add bx, [6]; bx = 

push ax; sp = ; written mem addr: , content:
push bx; sp = ; written mem addr: , content:
pop ax; sp = ; ax = 
pop bx; sp = ; bx =

push [4]; sp = ; written mem addr: , content:
push [6]; sp = ; written mem addr: , content:
```
# (2) 
