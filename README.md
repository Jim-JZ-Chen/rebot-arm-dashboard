# ReBot Arm 纯前端仪表盘

ReBot Arm（RS Lite）机械臂的浏览器端可视化仪表盘。**支持纯前端模式**——无后端也能完整体验 3D 可视化与前端 IK 演示。

## 功能

- Vue 3 + Three.js 实时 3D 机械臂渲染（URDF + OBJ 极简模型）
- 纯前端模式：未连接后端时自动启用本地 mock 状态，前端 IK 直接驱动 3D 模型
- 演示与路径编辑：画矩形 demo、抓取放置 demo，支持新建 / 导入 / 导出 / 编辑
- 目标点面板、关节状态、TCP 位姿、点动控制
- 系统控制面板：MoveIt 仿真 / Servo / 实体臂驱动等进程管理（需配合后端）

## 说明

- 原始项目：<https://gitee.com/dfjhde/rebot-arm>（ROS2 Jazzy，Ubuntu 24.04）
- 本仓库仅包含前端构建产物与 3D 资源，可直接部署到任意静态托管（GitHub Pages / Vercel / Nginx）
- 3D 模型为极简 OBJ（共约 52KB），整站体积不到 1MB
- WebSocket 连接已加容错：无后端时页面正常渲染，顶栏显示「未连接」
- 连接真实机械臂需配合原项目的 dashboard 后端（`ws://<host>/ws`）

## 本地预览

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```
