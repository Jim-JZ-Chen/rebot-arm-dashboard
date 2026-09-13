# ReBot Arm 纯前端仪表盘

ReBot Arm（RS Lite）机械臂的浏览器端可视化仪表盘，纯静态部署，无需后端即可打开预览。

## 功能

- Vue 3 + Three.js 实时 3D 机械臂渲染（URDF + STL）
- 系统控制面板：MoveIt 仿真 / Servo / 实体臂驱动等进程管理入口
- 前端 IK 解算演示：画矩形 demo、抓取放置 demo（仅驱动 3D 模型）
- TCP 位姿显示、关节状态、点动控制、Leap Motion 手势遥操作面板
- 解算参数面板（SolverPanel）、夹爪面板（GripperPanel）

## 说明

- 原始项目：<https://gitee.com/dfjhde/rebot-arm>（ROS2 Jazzy，Ubuntu 24.04）
- 本仓库仅包含前端构建产物与 3D 资源，可直接部署到任意静态托管（GitHub Pages / Vercel / Nginx）
- 3D 网格已做减面优化（66.8MB → 7MB），STL 转为 ASCII 格式
- WebSocket 连接已加容错：无后端时页面正常渲染，顶栏显示「未连接」
- 连接真实机械臂需配合原项目的 dashboard 后端（`ws://<host>/ws`）

## 本地预览

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```
