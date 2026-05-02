#FireGuard智能控制中心

**FireGuard—一款融合温度、湿度、烟雾、气体及多源环境数据的智能火灾风险感知与早期预警平台。

## What is this?

FireGuard is an intelligent fire early warning system designed for small and medium-sized venues (laboratories, dormitories, warehouses, shops, electrical rooms). It continuously collects environmental data through WiFi infrared temperature sensors, combines multi-level warning algorithms with AI-powered analysis, and issues alerts during the smoldering phase — upgrading traditional "post-incident alarm" to "pre-incident prediction."

## Key Features

- 🌡️ **Multi-source Data Fusion** — Unified ingestion of temperature, humidity, smoke, and gas data
- 🚨 **Three-level Warning System** — Notice → Warning → Critical, with scene-specific threshold configuration- 🚨 **三级预警体系**— 通知 → 警告 → 严重，支持针对场景配置阈值
- 🤖 **AI-powered Analysis** — Integrates Chinese LLMs (Zhipu GLM, Qwen, DeepSeek, etc.) for automated risk assessment and emergency recommendations- 🤖 **人工智能驱动的分析**— 集成中文大语言模型（智普GLM、通义千问、DeepSeek等），实现自动化风险评估与应急建议
- 🏗️ **3D Digital Twin Visualization** — Three.js building scenes with risk focus, fire spread simulation, and historical playback-️**3D数字孪生可视化**— 使用Three.js构建以风险为重点的场景、火灾蔓延模拟及历史回放
- 📱 **Mobile PWA Support** — Works in mobile browsers, installable to home screen as a native-like app- 📱 **移动PWA支持**— 在移动浏览器中可用，可安装到主屏幕，呈现原生应用般的体验
- 🔐 **Invite Code Permission System** — Three-tier access: admin / member / basic user- 🔐 **邀请码权限系统**— 三级访问权限：管理员 / 成员 / 基础用户
- 📊 **Real-time Monitoring Dashboard** — ECharts visualization for sensor trends, spectrum monitoring, and alert streams- 📊 **实时监控仪表板**— ECharts可视化，用于传感器趋势、频谱监测和告警流
- 🔄 **Full Alert Lifecycle Management** — From trigger to resolution to AI analysis- 🔄 **完整告警生命周期管理**— 从触发到解决再到AI分析

## Tech Stack##技术栈

| Layer | Technology ||分层技术|技术|
|-------|-----------|
| Frontend | Vue 3 + Element Plus + ECharts + Three.js ||前端|Vue 3 + Element Plus + ECharts + Three.js|
| Backend | FastAPI + SQLAlchemy 2.0 + SQLite + slowapi ||后端|FastAPI + SQLAlchemy 2.0 + SQLite + slowapi|
| AI | Zhipu GLM / Qwen / DeepSeek / Baidu ERNIE / OpenAI ||AI|智普GLM / Qwen / DeepSeek / 百度ERNIE / OpenAI|
| Hardware | ESP32 + MLX90614 (compatible with all WiFi sensors) ||硬件|ESP32 + MLX90614（兼容所有WiFi传感器）|
| Mobile | Vue 3 + Element Plus + ECharts (PWA) ||移动端|Vue 3 + Element Plus + ECharts（PWA）|

## Quick Start##快速入门

👉 See [快速开始.md](./快速开始.md) for detailed setup instructions.

Get it running in 5 minutes: Install Node.js and Python → Install dependencies → Start backend → Start frontend → Open browser.

Default login credentials: `admin@example.com` / `123456`

> ⚠️ Default password is for local testing only. For production, set `DEFAULT_ADMIN_PASSWORD` in `.env`.

## Quick Start with Docker

If you have Docker installed, start the full stack with a single command:

```bash
docker-compose up -d
```

After startup:

- Frontend: http://localhost:3000
- Backend API docs: http://localhost:18889/docs

Stop services:

```bash
docker-compose down
```

## Project Structure

```
├── frontend/            # PC frontend source code
├── backend/             # Backend source code
│   ├── routers/         #   API route modules (9)
│   └── tests/           #   Unit tests (70 test cases)
│   ├── config.py        # Configuration & JWT & password utils
│   ├── deps.py          # FastAPI dependency injection
│   ├── cache.py         # In-memory cache
│   ├── models.py        # Pydantic request/response models
│   └── database.py      # SQLAlchemy models & DB setup
├── hardware_firmware/   # Sensor firmware (Arduino)
├── mobile-app/          # Mobile PWA frontend
├── docker-compose.yml   # Docker Compose config
├── CONTRIBUTING.md      # Contribution guide
├── CODE_OF_CONDUCT.md   # Code of conduct
├── SECURITY.md          # Security policy
└── LICENSE              # AGPL-3.0
```

## Community & Contributing

We welcome contributions of all kinds! Please read our guidelines:

- [Contributing Guide](./CONTRIBUTING.md) — How to submit Issues and Pull Requests
- [Code of Conduct](./CODE_OF_CONDUCT.md) — Community standards
- [Security Policy](./SECURITY.md) — How to report security vulnerabilities

## License

This project is licensed under [AGPL-3.0](./LICENSE). Commercial use with closed-source modifications is prohibited.

## Contact

- Email: 2551230793@qq.com
- For commercial licensing, please contact the lead author

> Copyright: Sichuan Vocational and Technical College — yangming, shahaigui, yanshiyi, qixuding | Contact: 2551230793@qq.com
























[English](README_en.md) | 中文[英语](README_en.md)| 中文[英语](README_en.md)| 中文[英语](README_en.md)| 中文



> ⚠️ **协议警告：AGPL-3.0，禁止公司闭源商用，个人/学校可自由使用**

# 火睛智控中心

**FireGuard Intelligent Control Center** — 集成温度、湿度、烟雾、气体与多源环境数据的智能火灾风险感知与预警平台。**FireGuard智能控制中心**— 集成温度、湿度、烟雾、气体与多源环境数据的智能火灾风险感知与预警平台。

## 这是什么？

火睛智控中心是一套面向中小型场所（实验室、宿舍、仓库、商铺、配电房）的智能消防预警系统。它通过 WiFi 红外测温传感器持续采集环境数据，结合分级预警算法和 AI 智能分析，在火灾阴燃阶段即可发出预警，将传统"事后报警"升级为"事前预判"。

## 核心功能

- 🌡️ **多源数据融合感知** — 温度、湿度、烟雾、气体统一接入，打破信息孤岛
- 🚨 **三级分级预警体系** — 提示→警告→紧急，按场景差异化配置阈值，精准分级
- 🤖 **AI 智能研判分析** — 对接国产大模型，自动生成风险概率评估与应急建议
- 🏗️ **3D 数字孪生可视化** — Three.js 构建建筑场景，支持风险聚焦、火灾蔓延模拟、历史回溯-️**3D数字孪生可视化**— Three.js构建建筑场景，支持风险聚焦、火灾蔓延模拟、历史回溯
- 📱 **移动端 PWA 支持** — 手机浏览器打开即用，可添加到主屏幕像原生 APP 一样运行
- 🔐 **邀请码权限体系** — 管理员/会员/基础用户三级权限，灵活管控
- 📊 **实时监控大屏** — ECharts 可视化，传感器趋势、频谱监控、预警流一站式呈现— ECharts可视化，传感器趋势、频谱监控、预警流一站式呈现
- 🔄 **预警全闭环管理** — 从触发到处置到 AI 分析，完整处置链路

## 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | Vue 3 + Element Plus + ECharts + Three.js |
| 后端 | FastAPI + SQLAlchemy 2.0 + SQLite + slowapi |
| AI | 智谱GLM / 通义千问 / DeepSeek / 文心一言 / OpenAI |
| 硬件 | ESP32 + MLX90614（兼容所有 WiFi 传感器） |
| 移动端 | Vue 3 + Element Plus + ECharts（PWA） |

## 快速开始

👉 详见 [快速开始.md](./快速开始.md)

5 分钟本地跑起来：装好 Node.js 和 Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：安装Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：装好Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：安装Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：装好Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：安装Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：装好Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。5分钟本地跑起来：安装Node.js和Python → 安装依赖 → 配置环境变量 → 启动后端 → 启动前端 → 浏览器打开。

## 目录结构

```
├── frontend/            # PC端前端源码
├── backend/             # 后端源码
│   ├── routers/         #   API路由模块（9个）
│   └── tests/           #   单元测试（70个用例）
├── mobile-app/          # 移动端PWA源码
├── hardware_firmware/   # 传感器固件（Arduino）
├── .github/             # CI/CD + 社区模板
├── docker-compose.yml   # Docker一键部署
├── 启动系统.py           # 一键启动脚本
├── LICENSE              # AGPL-3.0 协议
├── README.md            # 本文件
├── 快速开始.md           # 5分钟上手指南
├── 系统介绍.md           # 功能详解
├── 部署指南.md           # 生产环境部署
├── 硬件接入指南.md       # 传感器接入教程
├── 功能配置手册.md       # AI/阈值/权限/环境变量配置
├── 常见问题.md           # FAQ
├── 开源协议说明.md       # AGPL 大白话解读
├── 目录结构说明.md       # 文件说明
└── 移动端使用指南.md     # 手机端教程
```

## 联系方式

- 邮箱：2551230793@qq.com
- 如需商业授权，请联系第一作者

## 快速体验（Docker）

如果你已安装 Docker，一条命令即可启动全栈：

```bash
docker-compose up -d
```

启动后访问：

- 前端界面：http://localhost:3000
- 后端 API 文档：http://localhost:18889/docs

停止服务：

```bash
docker-compose down
```

## 社区与贡献

我们欢迎任何形式的贡献！请阅读以下指南：

- [贡献指南](./CONTRIBUTING.md) — 如何提交 Issue 和 Pull Request
- [行为准则](./CODE_OF_CONDUCT.md) — 社区行为规范
- [安全策略](./SECURITY.md) — 安全漏洞报告方式



## 版权声明

本项目著作权归以下作者共同所有：
-第一作者：四川职业技术学院 杨明
-其他作者：四川职业技术学院 沙海贵、严世毅、戚旭丁

未经作者书面许可，禁止删除、篡改本版权声明。联系邮箱：2551230793@qq.com

---

> 版权所有：四川职业技术学院 yangming、shahaigui、yanshiyi、qixuding | 联系：2551230793@qq.com
