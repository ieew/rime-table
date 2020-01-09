# rime-table-decompiler

反編譯 Rime 的 ``xxx.table.bin`` 二進制詞典文件。

## 簡介

本項目 Fork 自 [whjiang/rime_table_bin_decompiler]。

相對於原項目，本項目有以下的更改。

+ 修復在 Linux 系統上的編譯錯誤
+ 更易讀的 README

本項目用於簡單的反編譯 Rime 的 ``xxx.table.bin`` 二進制詞典文
件，以生成 ``xxx.dict.yaml`` 源純文本詞典文件。

需要注意的是，由於 ``xxx.table.bin`` 二進制詞庫文件沒有元數據
信息，所以生成的 ``xxx.dict.yaml`` 源純文本詞典文件的文件頭中
的元數據信息是根據常見的元數據信息填補進去的，所以可能是錯誤
的，需要用戶自行修正。

## 使用

#### 安装工具鏈

+ GNU toolchain
+ CMake
+ Boost

#### 編譯

1. ``cmake .``
2. ``make``

## 用法

反編譯二進制詞庫並標準輸出。

```Bash
./rime_table_bin_decompiler xxx.table.bin
```

反編譯二進制詞庫並輸出到純文本詞庫文件中。

```Bash
./rime_table_bin_decompiler xxx.table.bin > xxx.dict.yaml
```



[whjiang/rime_table_bin_decompiler]: https://github.com/whjiang/rime_table_bin_decompiler
