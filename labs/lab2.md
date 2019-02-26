# (1) a check-off for mentioned theory of stack
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
# (2) a prologue to *interrupt*
> - 初始没有执行这段代码时，我们使用d命令观察2000:00内存，都是00，怎么创建栈结构指向这段内存时，我们发现有些数据了。这些数据是什么？
> - 我们发现这里面有cs值、ip值、ax值（这个容易看出来），还有bp值（00 00），还有flag的值（不容易发现）。
> - 为什么，**联想到操作系统的相关知识**，在讲内中断这章时，你就明白了。
> - t命令实际是引发了单步中断，执行中断例程时，CPU会将一些中断例程使用的的寄存器变量自动压栈到栈中，此例中就包括了上述的寄存器变量的值。
