# Daily-task
## 后端启动步骤（FastAPI + Uvicorn）
### 进入项目目录
     cd "E:\Microsoft VS Code\programs\aiXiv\aixiv-core"
### 激活外层虚拟环境
    ..\aixiv-venv-311\Scripts\activate
### 启动后端服务（需要开启docker）
     python -m uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
## 前端启动步骤
### 进入前端目录
    cd "E:\Microsoft VS Code\programs\aiXiv\aiXiv\ui"
### eg如果需要退出虚拟环境
     deactivate
### 启动开发服务
    npm start
