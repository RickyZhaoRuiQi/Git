
# Git

	- 为什么学习Git
		- 完整的版本控制功能，解决对人协作问题
		- 提高开发效率
		
	- 配置命令
		- git config --global user.name "xxx"		配置git全局用户名
		- git config --global user.name "xxx@xxx"	配置git全局邮箱
		- git config --list				查看配置信息
	
	- 仓库
		- 初始化版本库：git init
		- 添加文件到版本库：
			1. git add
			2. git commit
		- 查看状态：git status
	- Git工作流（模拟）
		- 工作区 -> 暂存区 -> 本地仓库 -> 远程仓库
		- 初始化git仓库：**git init**
		- 将文件放入暂存区：**git add file**
		- 将文件放入本地仓库：**git commit -m "xxx"**
		- 临时开发未做测试，将文件放入暂存区：**git add file**
		- 第二天，修改不需要，需要回滚：**git reset HEAD file**将暂存文件回滚到工作区  git checkout -- file清理工作区
		- 第二天的需求开发：git add file -> git commit -m "xxx"
		- 第二天的需求不需要，回滚到第一次：**git log**查看commit号 -> **git reset --hard commit号** 将仓库、暂存区和工作区的文件回到commit号的版本
		- 清理仓库：**git rm file**清空工作区文件  git commit -m "xxx"执行清空仓库
	- 远程仓库
		- ssh-keygen -t rsa -C "youremail@example.com" 创建SSH密钥
		- ssh -T git@github.com 测试是否连通
		- 添加远程仓库：*git remote add origin git@github.com:xxxxxxxx**
		- git pull origin master 拉取
		- git push -u origin master 
		- 克隆仓库：git clone git@github:xxxxxxx
	- 标签管理
		- 查看所有标签：git tag
		- 创建标签：git tag name
		- 指定提交信息：git tag -a name -m "xxx"
		- 删除标签：git tag -d name
		- 标签发布：git push origin name
	- 分支管理
		- 创建新分支：git branch xxx
		- 查看所有分支：git branch
		- 切换分支：git checkout xxx
		- 合并：get merge xxx 将xxx代码合并到当前分支
		- 删除分支：git branch -d xxx
