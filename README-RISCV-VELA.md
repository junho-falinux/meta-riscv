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

## Change linux kernel configuration

리눅스 커널 설정을 수정하려면 configuration fragment 파일을 추가하고, 리눅스 커널 레시피의 do_configure에서 merge_config.sh를 실행하도록 하면 됩니다.
recipes-kernel/linux/linux-yocto_%.bbappend, recipes-kernel/linux/linux-yocto/riscv-vela.cfg 참고.
