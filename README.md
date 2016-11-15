cctools
------
源码下载地址 [https://opensource.apple.com/tarballs/cctools/cctools-886.tar.gz](https://opensource.apple.com/tarballs/cctools/cctools-886.tar.gz)

这个工程包含了很多操作 mach-o 的工具，比如 nm, otool, strings, strip等。源码来自苹果的官网。但是苹果的源码是不能直接编译通过，做了如下的修改。

添加了以下文件:

1. dl_toolchain/usr/local/lib/libprunetrie.a 这个库来自苹果 ld64 项目
2. include/llvm-c/lto.h 这个文件来自 llvm 项目
3. include/mach-o/prune_trie.h 这个头文件来自 ld64 项目

### 编译

```
make
```

执行make后会在对应的目录下面生成以 .NEW 结尾的可执行文件

### 参考

ld64 [https://opensource.apple.com/source/ld64/](https://opensource.apple.com/source/ld64/)

llvm [http://llvm.org/](http://llvm.org/)