#git笔记（版本管理）

1. 上传一个项目到git仓库<font size=2> 
	- 在github上新建一个库,名字为xx
	- 本地终端cd到上传项目的目录中
	- git init(在本地初始化一个仓库)
	- git add -A(将所有的文件放到到本地仓库中，放一个文件是 git add 文件名（index.txt）)
	- git commit -m "first commit"(上传到git仓库前需要进行确认，－m是确认信息的变量，""内容是修改或者上传注释的内容，供其他开发者或者自己明白本次上传的文件大概是什么)
	- git push -u origin master(第一次和git仓库连接要关联)＋复制的地址（仓库地址）
	- (第一次链接还能)git remote add origin + 复制的地址
2. 修改本地仓库内容后提交到远程仓库
	- git status 查看项目有没有变动（假如其他人进行了上传更新项目的话）
	- git add + 新增文件
	- git add . (提交所有更新和新增的文件到本地仓库)
	- git commit -m "更改注释"
	- git push 
3. 