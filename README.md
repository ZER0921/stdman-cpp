# stdman-cpp

由于manpage文件是以`std::vector::size`形式命名的，与代码中的调用形式不一致，因此并不适合通过在vim中设置keywordprg来查看。

后续考虑实现一个shell脚本`cppman`，在命令行中查看相应的manpage

```bash
# 标准形式
$ cppman std::vector
-> std::vector.3

$ cppman std::vector::size
-> std::vector::size.3

# 支持自动添加命名空间std::
$ cppman vector
-> std::vector.3

# 支持使用函数调用符
$ cppman vector.size
-> std::vector::size.3

# 支持在复合文件中查询单个条目
$ cppman std::fgetc
-> std::fgetc,std::getc.3
```

