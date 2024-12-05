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

## Modify linux kernel source

리눅스 커널 소스를 수정하려면 build/tmp/work-shared/qemuriscv64/kernel-source에서 변경 사항을 적용합니다.
이 후 "kas shell kas/riscv-vela.yml" 명령으로 kas shell을 실행하고, 다음 명령으로 커널을 다시 빌드합니다.

```
bitbake -f -c compile linux-yocto
bitbake linux-yocto
```
QEMU를 다시 실행하면 커널의 변경사항이 반영되어 있습니다.
