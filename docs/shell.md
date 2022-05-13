# Shell

## 常用命令

cd、ls、pwd、echo、mv、rm、mkdir、rmdir

### 想做什么

```bash
date
```

> Fri May 13 12:15:07 PM CST 2022

```bash
echo hello
echo hello > hello.txt
echo hello >> hello.txt
cat < hello.txt
cat < hello.txt > hello2.txt
```
> hello

第 2 个命令：如果`hello.txt`不存在，新建后插入`hello`；如果存在用`hello`替换文件内容。

第 3 个命令：与第 2 个命令类似，唯一的区别在于，如果目标文件存在，不会覆盖文件内容，会在原来文本后附上`hello`。

Shell 通过环境变量搜寻可执行程序。`$PATH`、相对绝对路径、`ls`、`pwd`、`cd`。

```bash
cd -
```

切换目录（2个）

```bash
drwxr-xr-x
```

权限解释：

1. 第一个字符表示是否是目录、软链接。
2. 第二到四个字符表示当前用户的权限（是否可读、可写、可执行）。
3. 第五到七个字符表示当前组的权限（是否可读、可写、可执行）。
4. 最后三个字符表示除了当前用户和组以外的其他用户和组的权限。

Input stream、output stream。

`tee` 能够把输入输出 并把输出导入文件中。

## 管道 `|`

```bash
ls -l | tail -n1
```

## root user

```bash
sudo su
```

`su`: super user
