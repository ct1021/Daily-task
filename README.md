# Aixiv
## 后端启动步骤（FastAPI + Uvicorn）
### 进入项目目录
     cd "E:\Microsoft VS Code\programs\aiXiv\backend"
### 激活外层虚拟环境
    ..\aixiv-venv-311\Scripts\activate
### 启动后端服务（需要开启docker）
     uvicorn app.main:app --host 0.0.0.0 --port 35001 --reload
## 前端启动步骤
### 进入前端目录
    cd "E:\Microsoft VS Code\programs\aiXiv\frontend\ui"
### eg如果需要退出虚拟环境
     deactivate
### 启动开发服务
    npm start
## 提交数据库相关修改
### 确定本地仓库存在（确保里面有 .git 文件夹，说明这是一个 Git 仓库。）
     cd E:\Microsoft VS Code\programs\aiXiv\backend\aixiv-backend
### 检查/设置远程仓库地址
     git remote -v
### 如果远程地址不是 git@github.com:aixiv-org/aixiv-backend.git
     git remote set-url origin git@github.com:aixiv-org/aixiv-backend.git
### 测试 SSH 是否连通(Hi ct1021! You've successfully authenticated, but GitHub does not provide shell access.)
     ssh -T git@github.com
### 拉取远程最新分支
     git fetch origin 
     git push -u origin dev_tt# 或者你要基于的分支
     remote: Create a pull request for 'dev_tt' on GitHub by visiting:
     remote:   https://github.com/aixiv-org/aixiv-backend/pull/new/dev_tt
### 提交本地修改
     git add .
     git commit -m "描述本次修改"
### 推送到远程仓库
     git push -u origin dev_tt
     git push
### 确认推送成功
     git branch -vv
## 在 GitHub 上发起 Pull Request
     1. 打开提示的链接
     2. 填写 标题 和 描述
     Title: feat: update DB scripts and add db tests
     Description: 说明修改内容（数据库脚本、配置优化、新增测试等），以及本地测试情况。
     3. 点击 Create Pull Request 提交审核。
## 链接数据库
     mysql -h rm-bp18380uret3eh8n8ro.mysql.rds.aliyuncs.com -P 3306 -u huxiang -p
     然后输入密码 S7RFUcpp6HnSTe8Y
