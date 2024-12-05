# Quick Start

## Kas build

```
kas build kas/riscv-vela.yml
```

## Running in QEMU

Run kas shell.

```
kas shell kas/riscv-vela.yml

```

Run the 64-bit machine in QEMU.

```
MACHINE=qemuriscv64 runqemu nographic
```

To exit QEMU enter Ctrl+A+X.
