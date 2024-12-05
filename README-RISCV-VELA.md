# Quick Start

## Kas build

KAS is a Python-based tool designed to automate Yocto-based builds.
See [https://kas.readthedocs.io/](https://kas.readthedocs.io/)

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
