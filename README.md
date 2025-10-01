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
### 克隆仓库（使用 SSH 链接克隆官方仓库（推荐 SSH，避免 push 权限问题））
     git clone git@github.com:aixiv-org/aixiv-backend.git
     cd aixiv-backend
### 创建并切换到开发分支，避免在 main 上直接修改，创建新分支（如 dev_tt）
     git checkout -b dev_tt
### 本地修改 & 提交
     git add .
     git commit -m "feat: update DB scripts, config, add db tests"
### 推送分支到远程 把本地 dev_tt 分支推送到远程仓库，成功后终端会输出：：
     git push -u origin dev_tt
     remote: Create a pull request for 'dev_tt' on GitHub by visiting:
     remote:   https://github.com/aixiv-org/aixiv-backend/pull/new/dev_tt
## 在 GitHub 上发起 Pull Request
     1. 打开提示的链接
     2. 填写 标题 和 描述
     Title: feat: update DB scripts and add db tests
     Description: 说明修改内容（数据库脚本、配置优化、新增测试等），以及本地测试情况。
     3. 点击 Create Pull Request 提交审核。
## 链接数据库
     mysql -h rm-bp18380uret3eh8n8ro.mysql.rds.aliyuncs.com -P 3306 -u huxiang -p
     然后输入密码 S7RFUcpp6HnSTe8Y
