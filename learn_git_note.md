## 学习git的笔记

### 1.基本使用方法和流程
- git init 将本地文件初始化为一个git仓库
- git add <files> 添加一个文件 
- git commit -m "修改信息" 提交 暂存区文件到本地仓库
- git status 查看git 状态 
- git remote add origin <git@github.com:maxliubl/learngit.git>
- git push -u origin master 初次提交git 仓库到远程服务器上
### [注]
- git log 查看提交日志[最近到最远]
- git add . 添加本目录下的所有文件到　暂存区
- git ls-files 查看版本库中管理的文件
- git push origin master 后面推送不必使用 -u 参数

### 2.回退、修改、撤销、删除 恢复
#### 回退　历史未来版本
- git reset --hard HEAD^ 回退到上一个版本 上上个为：HEAD^^ ,往上100个版本:HEAD~100
- git reflog 命令日志
- git reset -- <commit id> 回到未来指定版本
#### 修改
- git diff HEAD --readme.md 查看工作区和版本库里最新版本的区别，修改
#### 撤销
- git checkout -- file 撤销工作区修改 或　丢弃工作区修改
- git reset HEAD file  撤销暂存区修改 
#### 删除
- rm rf file 删除工作区文件
- git rm file 删除版本库中文件
- git commit -m "" 提交删除修改到暂存区
- git checkout -- file 删错了，版本库存在file 可恢复到最新版本
#### 恢复
- git checkout -- filename 恢复版本库中文件到工作区

### 3.分支管理
#### Git鼓励大量使用分支：

- 查看分支：git branch
- 创建分支：git branch <name>
- 切换分支：git checkout <name>或者git switch <name>
- 创建+切换分支：git checkout -b <name>或者git switch -c <name>
- 合并某分支到当前分支：git merge <name>
- 删除分支：git branch -d <name>

### 4.标签管理
- 命令git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；
- 命令git tag -a <tagname> -m "blablabla..."可以指定标签信息；
- 命令git tag可以查看所有标签。``

- 命令git push origin <tagname>可以推送一个本地标签；
- 命令git push origin --tags可以推送全部未推送过的本地标签；
- 命令git tag -d <tagname>可以删除一个本地标签；
- 命令git push origin :refs/tags/<tagname>可以删除一个远程标签。











