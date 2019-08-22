在xcode中
1、自定义代码片段(codesinippets)，默认文件夹是： 
```~/Library/Developer/Xcode/UserData/CodeSnippets/```

2、系统代码片段(codesinippets），默认文件夹是：
```/Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources/SystemCodeSnippets.codesnippets```


我们可以从github上下载codesnippets项目，然后设置个软链链接到自定义codesinippets目标文件夹。

终端执行 `setup_snippets.sh` 脚本文件，实现软连接到自定义codesinippets目标文件夹。

脚本语言：
```
#! /bin/bash
mv ~/Library/Developer/Xcode/UserData/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets.backup

#rm ~/Library/Developer/Xcode/UserData/CodeSnippets

SRC_HOME=`pwd`
ln -s ${SRC_HOME}/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
echo "done"

```
