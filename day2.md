# 文件压缩

---

## 单文件压缩

- gzip 指令
  - 一般的压缩 方法。有个压缩级别，9 为最好，默认为 6，6 就可以。

```bash
gzip -k 文件名   保留源文件
```

- zcat、zless、zmore 即为压缩文件中的 cat less more
- egrep 为压缩文件中的查找数据，相当于替代了解开压缩文件并 grep 这个方法
- bzip2 比 gzip 压缩比更高，并且指令几乎相同，但压缩时间相对更久一些。同样也存在 bacat、bzmore、bzless、bzgrep 这些指令。
- xz 比 bzip2 压缩比更高。不过时间更久。同样也存在 xzcat、xzmore、xzless、xzgrep 这些指令。

## 打包： **_tar 指令_**

```
# 压缩格式
tar -J  压缩为xzg格式
    -j  压缩为bzip2格式
    -z  压缩为gzip格式

# 建议-f命令单独写
tar -f file 压缩文件名

tar -v  显示文件名
tar -a  追加文件
```
