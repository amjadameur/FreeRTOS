# Dump SEGGER via GDB

```
(gdb) set $SEGGER_BUF_BASE = _SEGGER_RTT.aUp[1].pBuffer
(gdb) set $SEGGER_BUF_SIZE = _SEGGER_RTT.aUp[1].WrOff
(gdb) set $SEGGER_BUF_END = $SEGGER_BUF_BASE + $SEGGER_BUF_SIZE
(gdb) dump binary memory segger-trace.bin ($SEGGER_BUF_BASE) ($SEGGER_BUF_END)
```