# rime_table_decompiler

反编译 Rime 的 ``xxx.table.bin`` 二進制詞典文件。

## 簡介

本項目 Fork 自 [whjiang/rime_table_bin_decompiler](https://github.com/whjiang/rime_table_bin_decompiler)。

相對於原項目，本項目有以下的更改。

+ 修復在 Linux 系統上的編譯錯誤
+ 更易讀的 README

本项目用于简单的反编译 Rime 的 ``xxx.table.bin`` 二進制詞典文件，
以生成 ``xxx.dict.yaml`` 源純文本詞典文件。

需要注意的是，由於 ``xxx.table.bin`` 二進制詞庫文件没有元数据信息，
所以生成的 ``xxx.dict.yaml`` 源純文本詞典文件的文件头中的元数据是根据常见的元数据填補进去的，
所以可能是错误的，需要用户自行修改。

## 编译方法

#### 工具鏈

+ GNU toolchain
+ CMake
+ Boost

#### 編譯

```Bash
cmake .

make
```

## 用法

```Bash
./rime_table_bin_decompiler xxx.table.bin > xxx.dict.yaml
```
