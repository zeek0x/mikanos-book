# 4.1 make入門 (osbook_day04a)

```console
$ cd $HOME/workspace/mikanos/kernel
$ git checkout osbook_day04a
$ source $HOME/osbook/devenv/buildenv.sh
```

- LDFLAGS に `-z separete-code` を追加

```diff
diff --git a/kernel/Makefile b/kernel/Makefile
index 2726448..1e1f524 100644
--- a/kernel/Makefile
+++ b/kernel/Makefile
@@ -3,7 +3,7 @@ OBJS = main.o

 CXXFLAGS += -O2 -Wall -g --target=x86_64-elf -ffreestanding -mno-red-zone \
             -fno-exceptions -fno-rtti -std=c++17
-LDFLAGS  += --entry KernelMain -z norelro --image-base 0x100000 --static
+LDFLAGS  += --entry KernelMain -z norelro -z separate-code --image-base 0x100000 --static


 .PHONY: all
```

ビルドし、実行が可能

```
$ make
$ cd $HOME/edk2
$ build
$ $HOME/osbook/devenv/run_qemu.sh Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi $HOME/workspace/mikanos/kernel/kernel.elf
```

画面は変わらないので省略
