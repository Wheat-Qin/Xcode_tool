在xcode中，自定义codesinippets默认文件夹是 ~/Library/Developer/Xcode/UserData/CodeSnippets/
系统codesinippets默认文件夹是
/Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources/SystemCodeSnippets.codesnippets
那我们就可以从git上下载codesnippets项目，然后设置个软链链接到自定义codesinippets目标文件夹。
#! /bin/bash
mv ~/Library/Developer/Xcode/UserData/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets.backup

#rm ~/Library/Developer/Xcode/UserData/CodeSnippets

SRC_HOME=`pwd`
ln -s ${SRC_HOME}/CodeSnippets ~/Library/Developer/Xcode/UserData/CodeSnippets
echo "done"

作者：_冷忆
链接：https://www.jianshu.com/p/8b4eee622293
来源：简书
简书著作权归作者所有，任何形式的转载都请联系作者获得授权并注明出处。
