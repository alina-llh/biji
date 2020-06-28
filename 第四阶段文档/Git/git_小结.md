# 笔记

## 今日大纲
* 复习
* GitHub 介绍与注册
* 本地仓库推送到远程仓库
* 仓库克隆
* GitHub 多人开发配置（组织创建）
* 免密登录（SSH）
* GitFlow 介绍
* GitHub 网页功能
* 码云
* GitLab
* VSCode
* Markdown

## git 清理缓存的账号和密码
```
git credential-manager uninstall
```
## Github的提交注意点
1. 本地仓库一定要有提交历史
2. 使用 https 协议的链接提交

## git remote 命令用来管理远程仓库
git remote add 添加远程仓库(实质上是添加远程仓库 URL 的别名)

git remote add origin https://github.com/xiaohigh/test2.git  
* origin 就是别名(小名)
* https://github.com/xiaohigh/test2.git  就是完整形式(大名)

git remote -h 查看使用帮助
* git remote add    添加
* git remote remove 移除
* git remote rename 重命名

## git push
git push 将本地仓库的某个分支推送到远程仓库
```
git push -u origin master
```
* -u 关联(第一次加 u 之后建立分支链接, 后续可以直接使用 git push 进行提交)
* origin 远程仓库的别名
* master 本地的分支名

## 仓库克隆是将远程的所有分支都拉回到本地

## clone 与 pull
* clone 是将整个仓库的内容都下载回来
* pull 是对指定的分支内容进行拉取

## 多人协作的流程
0. 创建组织, 并邀请组员加入
1. 组长创建一个**组织**的仓库
2. 组长创建一个本地仓库, 然后将本地仓库推送到组织新建的仓库中
3. 组员就可以克隆仓库, 然后对仓库的文件修改(添加,删除,重命名,修改文件内容)
4. 本地提交 git add -A     git commit -m "注释"
5. 提交 git push

## 推送习惯
每次使用 push 之前, 首先执行以下 pull.

## 练习
* 创建一个组织仓库
* 组员需要在仓库中创建一个名字为自己姓名的文件, 后缀为 html. eg: 玲慧.html  
* 创建完成后, 提交到远程仓库中.

## 注意点
1. 组织的权限一定要配置好. 否则提交会出现 403 
2. 关于克隆. 一定要在一个非Git仓库的文件夹下进行

## 远程仓库不一定是 GitHub 仓库

## markdown 
* typora 软件

## star 星星
欢迎 star, 欢迎 PR

## fork 叉子
复制别人的仓库

## pull request 
* 分支合并请求
* 将 fork 的仓库代码合并到原始的仓库的代码(开源代码贡献)

## GitLab
GitLab 是一个利用 Ruby on Rails 开发的开源应用程序，实现一个自托管的Git项目仓库，可通过Web界面进行访问公开的或者私人项目。 它拥有与 Github 类似的功能

## Git 总结

### git 命令
* git status
* git add -A
* git commit -m "注释"
* git branch 查看分支
* git checkout 切换分支
* git checkout -b 创建并切换分支
* git merge   合并分支
* git remote 
* git push 
* git pull

### 注意事项
1. 执行 git 命令的位置
2. 学会使用 git status 查看仓库的状态. 
3. commit 注意引号
4. 分支切换, 推送拉取, **一定要将当前分支的内容进行提交**
5. 关于 git push
   1. 简写 git push 
   2. 完整形式 git push origin master
6. git push 之前先做 pull 

### 出了问题才是自己提高的时候
英文提示类的问题, 首先先翻译 (有道翻译)










