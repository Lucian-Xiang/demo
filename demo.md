# 参考文献：

[Github——git本地仓库建立与远程连接（最详细清晰版本！附简化步骤与常见错误）_将本地仓库与远程仓库关联-CSDN博客](https://blog.csdn.net/qq_29493173/article/details/113094143)

### 1.1 建本地的版本库

等同于新建一个空文件夹
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/a78d95ac56b906c0b152bf6c89a7eef4.png)
进入，右键-Git Bash-输入“git init”初始化成一个Git可管理的仓库
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/9fa72196cbbecc2979ba1ec9288e74e5.png)
这时文件夹里多了个.git文件夹，它是Git用来跟踪和管理版本库的。
如果你看不到，需要设置一下让隐藏文件可见。 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d9705a9e548d8af0e3869be69181b6a7.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/96e9fa2147cac78d6e38b41164b48dc9.png)

### 1.2 源代码放入本地仓库

把项目/源代码粘贴到这个本地Git仓库里面
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/6299c7da779035b4c6ffc47630489574.png)
**git status：查看当前的状态**

- 红字表示未add到Git仓库上的文件
- 绿字表示已add到Git仓库上的文件

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/fcd8d08bb5a49c2a5464f4ada9136841.png)

然后通过**git add**把项目/源代码添加到仓库
（“git add .” ：把该目录下的所有文件添加到仓库，注意点“.”）

可以看到，查询状态后文件已经变为绿色，说明add成功
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/401df6d019b96c24bbd28be3e5c11631.png)

### 1.3提交仓库

用**git commit**把项目提交到仓库。
-m 后面引号里面是本次提交的注释内容，可以不写，但最好写上，不然会报错

```javascript
git commit -m "first commit"
```

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/7c3b2b93c148ccd7089996f8230a0867.png)

5）关联远程仓库，输入以下命令进行关联远程仓库。

```
git remote add origin 远程仓库地址
```

其中远程仓库地址可在下图所示处找到

https://github.com/Lucian-Xiang/journal.git

6）推送代码

输入以下命令添加并提交到本地仓库，其中初始化项目为提交信息，表明这次提交做了什么内容。

```
git add --all
git commit -m "初始化项目"
```

继续提交到远程仓库

```
git push -u origin master
```





