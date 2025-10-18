# 13.2 コンテキストの切り替えに挑戦 (sobook_day13a)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day13a
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/13.2.png)

# 13.3 コンテキストスイッチの自動化 (osbook_day13b)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day13b
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

図は省略

# 13.4 マルチタスクの検証 (osbook_day13c)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day13c
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

図は省略

# 13.5 タスクを増やす (osbook_day13d)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day13d
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/13.5.png)
