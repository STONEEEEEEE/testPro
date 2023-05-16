# git 指令



### 1. 创建本地仓库

~~~
git init
~~~



### 2. 添加文件到暂存区

~~~
git add 文件名
~~~



### 3. 将暂存区文件提交到本地仓库

~~~
git commit -m "提交注释"
~~~

-m后面输入的是本次提交的说明，提交成功后会显示：

1 file changed：1个文件被改动（我们新添加的readme.txt文件）；

2 insertions：插入了两行内容（readme.txt有两行内容）。



为什么Git添加文件需要add，commit一共两步呢？因为commit可以一次提交很多文件，所以你可以多次add不同的文件



### 4. 关联本地仓库与远程仓库

~~~
git remote add origin 地址
git push -u origin main
~~~



### 5. 查看状态

```
git status
```



### 6. 版本回退

#### 回退历史版本

~~~
git reset --hard HEAD^
~~~

首先，Git必须知道当前版本是哪个版本，在Git中，用`HEAD`表示当前版本，也就是最新的提交`1094adb...`，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个`^`比较容易数不过来，所以写成`HEAD~100`。

#### 查看历史版本

~~~
git log
~~~

回退之前的那个版本已经看不到了，这时如果想回到之前那个版本，需要知道版本号，git内部有个指向当前版本的head指针，将指针从当前版本指回去，所以git回退版本特别快

#### 查看历史命令

~~~
git reflog
~~~

