# build / flash

assuming microbit:v2

`cargo embed --target thumbv7em-none-eabihf`

# debug

```
gdb target/thumbv7em-none-eabihf/debug/<file>
target remote :1337 (port running gdb stub)
```

some useful gdb commands

```
layout src/asm
tui disable

c / continue
next
break <name / linenum>
info break
delete <break>
info locals

monitor reset
```
