# Shell Tools and Scripting

```sh
$ foo=foer
$ echo "It's $foo"
It's foer
$ echo 'It is $foo'
It is $foo
```

注意彼此的区别。

一个功能更全的 mkdir+cd 函数：

```sh
mc () {
  mkdir -p "$1"
  cd "$1"
}
```

Shell 参数：

- `$0` \- Name of the script
- `$1` to `$9` \- Arguments to the script. `$1` is the first argument and so on.
- `$@` \- All the arguments
- `$#` \- Number of arguments
- `$?` \- Return code of the previous command
- `$$` \- Process identification number (PID) for the current script
- `!!` \- Entire last command, including arguments. A common pattern is to execute a command only for it to fail due to missing permissions; you can quickly re\-execute the command with sudo by doing `sudo !!`
- `$_` \- Last argument from the last command. If you are in an interactive shell, you can also quickly get this value by typing `Esc` followed by `.` or `Alt+.`

Shell globbing:

- 通配符
- `{}`

发现一个图片格式转换利器：`convert`，由 [imagemagick](https://en.wikipedia.org/wiki/ImageMagick) 提供。

运行 `sh script.py` 了以下文件，电脑死机了。

```py
#!/usr/bin/env python

import sys
for arg in reversed(sys.argv[1:]):
  print(arg)
```

Shell 脚本分析工具：[shellcheck](https://www.shellcheck.net/)。

[tldr](https://tldr.sh/) 工具。

ffmpeg 视频格式转换工具。

find 更丰富的文件/目录查找工具。[fd](https://github.com/sharkdp/fd): Simple, fast and user-friendly alternative to find.

locate 是哪个软件包的？

tree broot

hstr

take input from both arguments and STDIN: `ls | xargs rm`
