[quote="moling, post:1, topic:1496, full:true"]
高效命令行

基本单词

英文      | 翻译
----------|----------------|
directory | 目录、文件夹
file      | 文件
make      | 新建
remove    | 删除
move      | 移动
copy      | 复制
list      | 罗列
link      | 链接
find      | 查找
echo      | 发出回音、重复
touch     | 触摸

基本概念


没有盘符，整个硬盘就是 /，叫做 根目录

文件、目录、路径、节点

文件
目录，就是文件夹
当前目录，用 . 表示
父目录，用 .. 表示


节点 = 文件 或者 目录
路径
绝对路径，以 / 开头，能唯一确定一个节点如 /tmp/a/1.txt


相对路径，不以 / 开头，是一个相对值
如 a/, ./a/

如 b.txt, ./b.txt

如 a/b.txt, ./a/b.txt

如 ../c/d.txt








大部分事情，图形界面（GUI）能做，命令行也能做，只是方式不同
         | 输入     | 输出
---------|----------|------------|
图形界面 | 鼠标点击 | 弹出对话框
命令行   | 输入文字 | 输出文字以浏览网页为例：curl
为什么你觉得命令行难？
因为你用 Windows 用了十几年，学了十几年。
而用 Linux 的时间却是 0。
命令行的样子$ 命令 -选项缩写 --选项 参数
结果缩写1 程序员为了「输入方便」对命令进行缩写2 缩写规则是省略 A、E、I、O、U 五个元音字母，留下 2 到 3 个字母（有时会例外）
















 命令
全写
缩写 
 创建目录
make directory
mkdir 
 删除
remove
rm 
 移动 / 重命名
move
mv 
 复制
copy
cp 
 罗列
list
ls 
 链接
link
ln * 


* Windows 系统默认不支持链接

3 ~ 表示用户目录

假设你的用户名是 administrator，那么


在 Windows 系统，~ 表示 /Users/administrator/ 目录（一般在 C 盘）
在 Linux 系统，~ 表示 /home/administrator/ 目录


文件相关操作

操作             | 命令
-----------------|-----------------------|
进入目录         | cd
显示当前目录     | pwd
创建目录         | mkdir 目录名
创建目录         | mkdir -p 目录路径
--               | --
查看路径         | ls 路径
查看路径         | ls -a 路径
查看路径         | ls -l 路径
查看路径         | ls -al 路径
--               | --
创建文件         | echo '1' &gt; 文件路径
创建文件         | echo '1' &gt;! 文件路径
创建文件         | echo '1' &gt;&gt; 文件路径
创建文件         | touch 文件名
改变文件更新时间 | touch 文件名
--               | --
复制文件         | cp 源路径 目标路径
复制目录         | cp -r 源路径 目标路径
--               | --
移动节点         | mv 源路径 目标路径
--               | --
删除文件         | rm 文件路径
强制删除文件     | rm -f 文件路径
删除目录         | rm -r 目录路径
强制删除目录     | rm -rf 目录路径
--               | --
查看目录结构     | tree
建立软链接       | ln -s 真实文件 链接

* 永远不要运行 rm -rf /

技巧

操作                     | 命令
-------------------------|-------------------------------|
回到刚才的目录（返回）   | cd -
使用上一次的命令         | 上
使用上一次的命令         | !!
使用上一次的最后一个参数 | &lt;kbd&gt;alt&lt;/kbd&gt; + &lt;kbd&gt;.&lt;/kbd&gt;
一句话执行两个命令       | xxx; yyy
一句话执行两个命令       | xxx&& yyy

如何在命令里面打回车？

\后面接回车

什么时候加引号？

有空格等特殊字符的时候加引号

如何自学命令行


man ls
ls -h
ls --help
ExplainShell.com


使用 vim 编辑文件


如何退出 vim
按一下 ESC

依次按下 :wq，回车


如何输入i

如何学习 vim
vimtutor 



如何快速查找文件


Everything
find . -iname xxx -type d


什么是 ~/.bashrc

就是一个文件，bash 会在启动时运行 ~/.bashrc 里面的内容

添加 alias

在 ~/.bashrc 里面添加

alias xxx='yyy'

然后运行

source ~/.bashrc

如何使用 z


下载 z.sh
在 ~/.bashrc 里面加入
    source /path/to/z.sh
source ~/.bashrc


命令行与 GUI 融为一体


如何在命令行中调用 GUI
Windows: start . 或者 explorer .

macOS: open .



如何从 GUI 进入命令行Windows: 使用 Everything 查找文件，打开目录，右键，「Git Bash here」



游泳定律

学习游泳：


下水
不下沉（不死）


学习 bash：


使用 bash
不要被 bash 吓倒
[/quote]

