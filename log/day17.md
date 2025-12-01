# 17.4 ボリュームを読み出す (osbook_day17a)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day17f
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](img/17.4.png)
