# Dependencies
- [DOSBox](https://www.dosbox.com/), an x86 emulator with DOS
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
 - -r[register-name]: to read and write registers
 - -d [segment-address:offset-addr] [amount-of-displayed]: to display binary code in memory
 - -u [segment-address:offset-addr] [amount-of-displayed]: to display the disassembling result
 - -e [segment-address:offset-addr] [... ... ...]: to edit in memory
 - -a [segment-addr:offset-addr]: to write instructions into memory in the form of assembly code
 - -t: to execute the instruction pointed by CS:IP
