### GitLab

#### 创建项目

```
【New Project】
```

![1-创建项目](D:\个人发展\学习历程\StudyRoute\Git\GitLab\images\1-创建项目.png)

#### 设置

![2-项目设置](D:\个人发展\学习历程\StudyRoute\Git\GitLab\images\2-项目设置.png)

##### 设置成员

```
【Settings】-【Member】
```

##### 删除项目

```
【Settings】-【General】-【Advanced settings】-【Remove project】
```

#### 添加项目

##### 添加README

```shell
克隆远程仓库到本地
git clone git@47.106.216.108:branch-callspdb/Sbacn-Manage.git

进入本地仓库
cd Sbacn-Manage

创建README.md文件
touch README.md

添加到缓存
git add README.md

提交
git commit -m "add README"

推送到远程分支
git push -u origin master
```

##### 添加.gitignore

```shell
创建.gitignore文件
touch .gitignore

编辑.gitignore文件
vim .gitignore

设置git忽略文件
git config core.excludesfile .gitignore

添加到缓存区
git add .gitignore

提交
git commit -m "add .gitignore"

推送到远程
git push -u origin master
```

##### 上传项目

```shell
如果项目存在空文件夹，需要在每一个空文件夹中额外添加一个文件，（git无法提交空文件夹）

批量添加-所有空文件夹添加.gitkeep
find . -type d -empty -exec touch {}/.gitkeep \;

批量删除-删除所有gitkeep
find ./ -type f -name '.gitxxx' -delete


```

#### 扩展

##### .gitignore不生效

```shell
.gitignore只能忽略原来没有被跟踪的文件，跟踪过的文件是无法被忽略的。如果要忽略跟踪过的文件解决方法就是先把本地缓存删除（改变成未track状态），然后再提交:

删除缓存
git rm -r --cached .

添加到缓存
git add .gitignore

提交
git commit -m 'add .gitignore'
```





