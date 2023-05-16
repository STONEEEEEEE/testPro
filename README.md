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

#### 
