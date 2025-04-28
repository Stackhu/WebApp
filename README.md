一个基于FastAPI + Vue3开发的web应用

## 项目概述

- 🏗️ 现代 Web 应用的基础架构
- 📝 前后端分离开发模式
- ⚡ RESTful API 设计与实现
- 🔒 类型安全的代码实践
- ♻️ 完整的 CRUD 操作流程

## 系统架构

### 技术栈

#### 前端

- **框架**: Vue 3 + TypeScript
- **构建工具**: Vite
- **UI 组件**: Element Plus
- **状态管理**: Pinia
- **路由**: Vue Router
- **HTTP 客户端**: Axios
- **代码规范**: ESLint + Prettier

#### 后端

- **框架**: FastAPI
- **数据库**: SQLite
- **ORM**: SQLAlchemy
- **API 文档**: Swagger UI / ReDoc
- **类型检查**: Pydantic
- **CORS 支持**: CORSMiddleware

### 前后端交互流程

1. 数据流向

   ```
   Frontend (Vue.ts)             Backend (FastAPI)             Database (SQLite)
   +-----------+                   +------------+                +-----------+
   |           |  HTTP Request     |            |  SQL Query     |           |
   | UI        | ----------------> | REST API   | -------------> |  Tables   |
   |           | <---------------- |            | <------------- |           |
   +-----------+  JSON Response    +------------+  Query Result  +-----------+
   ```
2. 关键技术点说明

   - **类型安全**：前端 TypeScript + 后端 Pydantic 实现端到端类型检查
   - **状态管理**：Pinia 实现前端状态集中管理
   - **API 设计**：符合 RESTful 规范的 API 设计
   - **跨域处理**：CORS 中间件配置

## 项目结构

```
taskflow-web-app-demo/
├── frontend/              # 前端项目目录
│   ├── src/
│   │   ├── assets/        # 静态资源（logo.svg）
│   │   ├── components/    # 公共组件（PageContainer.vue）
│   │   ├── services/      # API 服务（api.ts, itemService.ts）
│   │   ├── stores/        # Pinia 状态管理（items.ts）
│   │   ├── types/         # TypeScript 类型定义（item.ts）
│   │   ├── views/         # 页面组件
│   │   │   ├── HomeView.vue
│   │   │   ├── ItemList.vue
│   │   │   ├── ItemCreate.vue
│   │   │   ├── ItemEdit.vue
│   │   │   ├── ItemDetail.vue
│   │   │   └── NotFound.vue
│   │   ├── App.vue        # 根组件
│   │   ├── main.ts        # 入口文件
│   │   └── router/        # 路由配置
│   ├── index.html
│   └── package.json       # 依赖配置
└── backend/               # 后端项目目录
    ├── app/               # 应用代码
    │   ├── models/        # 数据模型（item.py）
    │   ├── schemas/       # Pydantic 模型（item.py）
    │   ├── crud/          # 数据库操作（item.py）
    │   ├── database.py    # 数据库配置
    │   └── main.py        # 入口文件
    └── environment.yml    # Conda 环境配置
```

## 开发环境配置

### 环境要求

- Node.js >= 16
- Anaconda 或 Miniconda
- Git

### 快速开始

1. 克隆项目

```bash
git clone ...
```

2. 启动后端

```bash
cd backend

# 创建并激活 conda 环境
conda env create -f environment.yml
conda activate crud-app

# 启动服务
python -m uvicorn app.main:app --reload
```

3. 启动前端

```bash
cd frontend

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

4. 访问应用

- 前端页面：`http://localhost:5173`
- API 文档：`http://localhost:8000/docs`

#### 常见问题

1. 如果遇到 conda 安装包失败，可以尝试：
   ```bash
   # 添加 conda-forge 源
   conda config --add channels conda-forge
   # 重试安装
   conda env create -f environment.yml
   ```
2. 如果遇到 Node 版本问题，可以尝试：
   ```bash
   # 安装 node
   nvm install --lts
   # 设置 node 版本
   nvm use --lts
   ```

## 学习资源

- [Vue 3 官方文档](https://vuejs.org/guide/introduction.html)
- [FastAPI 官方文档](https://fastapi.tiangolo.com/)
- [Element Plus 官方文档](https://element-plus.org/)
- [Pinia 官方文档](https://pinia.vuejs.org/)
- [Vue Router 官方文档](https://router.vuejs.org/)
- [Axios 官方文档](https://axios-http.com/)
- [FastAPI 全栈模板（官方示例）](https://github.com/fastapi/full-stack-fastapi-template)

## 联系方式

- 项目链接: [https://github.com/Stackhu/WebApp](https://github.com/Stackhu/WebApp)
- 作者邮箱: [1481707546@qq.com](mailto:1481707546@qq.com)

## 致谢

特别感谢：
- 复旦大学软件工程课程的所有师生及第五小组成员们对项目的支持




