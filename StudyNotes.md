Git与GitHub实践学习笔记

基本信息 
姓名：訾智雯
学号：202111680067
GitHub账号：ciyan-evan
实践时间：2025年5月

一、核心学习内容
1. Git版本控制系统
- 分布式版本管理：每个开发者拥有完整仓库副本
- 三大工作区域：
- 工作目录（Working Directory）
- 暂存区（Staging Area）
- Git仓库（Repository）
- 关键特性：版本回溯、分支管理、协作开发
2. GitHub平台
- 代码托管服务
- 协作开发功能：
- Pull Request
- Issue跟踪
- Actions自动化

二、详细实践记录
1. 开发环境搭建
#验证安装
$ git --version

git version 2.49.0.windows.1

#基础配置
$ git config --global user.name "訾智雯"
$ git config --global user.email "2152601592@qq.com"

2. 完整工作流实践

2.1. 仓库初始化
mkdir my-project && cd my-project
git init

2.2. 首次提交
echo "Hello Git!" > hello.txt
git add hello.txt
git commit -m "feat: 添加初始文件"

2.3. 远程协作
git remote add origin https://github.com/ciyan-evan/my-first-repo.git
git push -u origin main

2.4. 变更管理示例
#第二次提交（修改文件）
echo "Hello Git v2!" > hello.txt
git diff  # 查看变更
git commit -am "fix: 更新问候语"
#第三次提交（新增功能）
echo "print('Hello')" > main.py
git add .
git commit -m "feat: 添加Python脚本"

2.5.更改到远程仓库
git push origin main

三、问题解决

问题现象：src refspec main does not match	错误原因：分支命名冲突	解决方案：git branch -m master main

问题现象：remote origin already exists	错误原因：分支命名冲突重复添加远程仓库	解决方案：git branch -m master maingit remote set-url origin [url]

四、实践心得
1. 版本控制优势验证
- 通过git checkout <commit-id>成功回退到历史版本
- 使用git branch feature-1实现功能隔离开发
- git merge体验代码合并过程
2. GitHub核心价值
- 成功部署GitHub Pages个人页面
- 通过Fork+Pull Request参与开源项目
- 使用Issue管理开发任务

五、学习成果
✅ 成功完成5次规范提交
✅ GitHub仓库正常同步
✅ 掌握基础协作流程


最后更新：2025年5月1日
仓库地址：My-First-Repo

