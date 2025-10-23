# 14.1 スリープしてみる (osbook_day14a)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day1
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```
