# Getting started with System Information on Mbed OS

This guide reviews the steps required to get system information on Mbed OS platform.

Please install [mbed CLI](https://github.com/ARMmbed/mbed-cli#installing-mbed-cli).

## Import the example application

From the command-line, import the example:

```
mbed import mbed-os-example-sys-info
cd mbed-os-example-sys-info
```

### Now compile

Invoke `mbed compile`, and specify the name of your platform and your favorite toolchain (`GCC_ARM`, `ARM`, `IAR`). For example, for the ARM Compiler 5:

```
mbed compile -m K64F -t ARM
```

Your PC may take a few minutes to compile your code. At the end, you see the following result:

```
[snip]
+------------------+-------+-------+------+
| Module           | .text | .data | .bss |
+------------------+-------+-------+------+
| [lib]\c_w.l      | 11473 |    16 |  348 |
| [lib]\cpprt_w.l  |    36 |     0 |    0 |
| [lib]\fz_wm.l    |    18 |     0 |    0 |
| [lib]\m_wm.l     |    48 |     0 |    0 |
| anon$$obj.o      |    32 |     0 | 1024 |
| main.o           |   136 |     0 |    0 |
| mbed-os\drivers  |   130 |     0 |    0 |
| mbed-os\features |   132 |     0 |  304 |
| mbed-os\hal      |  1660 |    30 |   64 |
| mbed-os\platform |  3465 |   104 |  604 |
| mbed-os\rtos     | 12926 |  2310 | 4592 |
| mbed-os\targets  |  9193 |   104 |  324 |
| Subtotals        | 39249 |  2564 | 7260 |
+------------------+-------+-------+------+
Total Static RAM memory (data + bss): 9824 bytes
Total Flash memory (text + data): 41813 bytes

Image: .\BUILD\K64F\ARM\mbed-os-example-sys-info.bin
```

### Program your board

1. Connect your Mbed device to the computer over USB.
1. Copy the binary file to the Mbed device.
1. Press the reset button to start the program.
