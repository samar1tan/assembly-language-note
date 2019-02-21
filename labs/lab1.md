# Dependencies
- [DOSBox](https://www.dosbox.com/), a cross-platform x86 emulator with DOS
- debug.exe (download it from any download site)
# Configuration
1. move `debug.exe` into wherever accessible like `D:\`
2. open `DOSBox` and execute the following commands
3. mount the disk containing `debug.exe`:
```cmd
Z:\>mount d d:\
```
4. switch to the selected directory:
```cmd
Z:\>d:\
```
5. enjoy it:
```cmd
D:\>debug
```
# Summary: Used Commands
- To monitor registers
    - -r[register-name]: read and write registers
- To display memory
    - -d [segment:offset] [display-amount]: binary code
    - -u [segment:offset] [display-amount]: the disassembling result
- To edit memory
    - -e [segment:offset] [... ... ...]: with numbers or ASCII char/string
    - -a [segment:offset]: with assembly code
- To execute
    - -t: the instruction pointed by CS:IP
