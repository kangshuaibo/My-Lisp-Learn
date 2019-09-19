#实用Common Lisp编程
peter Seibel著   
田春 译    

- 它是人类历史上第二个高级程序设计语言（第一个是fortran）
- 人工智能专家发表重大意义第一篇lisp论文
- 拓展阅读《黑客与画家》


###1、环境配置：  
- Macports网站左侧的链接，进入 Installing MacPorts 。 
- 找到最简单的 “Mac OS X Package (.pkg) Installer”，按照指引下载pkg文件，双击进行安装。
- 进入mac的终端界面输入：```port help selfupdate```测试macports是否正常
- 升级一下```sudo port selfupdate```
- 然后输入```port search clisp```，确认clisp可用。 
- 运行```sudo port install clisp```就开始安装了
- 输入了“clisp”，期待已久的界面终于出现！ 


###2、sublime配置：
- 确保上述环境安装好
- command+shift+p调出界面，输入install package
- 进入后输入sublimeREPL安装
- 成功
- sublime上方Tools出现SublimeRELP,依次选择SublimeREPL->Common Lisp->Gun Clisp进入开发界面

###3、基本使用：
```
新建power.lisp文件 写入以下内容：
(defun power (x y) (if (= y 0) 1 (* x (power x (1- y))))) 

```
注意保存路径问题：把.lisp文件可以放到桌面  
在终端中cd 到文件夹，再输入clisp

```
终端中操作：
mikasa:~ kangshuaibo$ cd ~/Desktop/My-Lisp-Learn   
mikasa:My-Lisp-Learn kangshuaibo$ clisp
```

```

[1]> (load "power.lisp")	//在终端中只打出这一句 后面为运行时生成
;; Loading file power.lisp ...
;; Loaded file power.lisp
T
[2]> (power 3 4)		//调用函数传递参数
81
[3]> 

```

###基本语法：



