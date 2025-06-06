# 12.1 FADT を探す (osbook_day12a)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12a
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

画面は変わらないので省略

# 12.2 ACPI PM タイマを使う (osbook_day12b)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12b
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/12.2.png)

# 12.3 USB キーボードドライバ (osbook_day12c)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12c
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/12.3.png)

# 12.4 モディフィアキー (osbook_day12d)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12d
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/12.4.png)

# 12.5 テキストボックス (osbook_day12e)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12e
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/12.5.png)

# 12.6 カーソル (osbook_day12f)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day12f
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

![](./img/12.6.png)
