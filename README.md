# LXDAO Co-Learning: Reactive dApp

学习 Reactive Network 并掌握开发睿应式智能合约（Reactive Smart Contracts）的共学项目。

## 学习目标

- 理解 Reactive 与传统 EVM 的根本区别
- 掌握事件驱动的智能合约开发模型
- 实现跨链自动化 dApp
- 参与 Casual Hackathon 并完成项目

---

## Phase 1: 理解 Reactive 思维

### 学习目标

- 理解 Reactive 与传统 EVM 的根本区别
- 掌握核心架构：ReactVM + Reactive Network 环境
- 理解"事件驱动智能合约"（Reactive Smart Contracts）
- 了解 Reactive 适合解决什么问题

### 学习材料

| 资源 | 链接 |
|------|------|
| Reactive Network 官网 Overview | https://reactive.network/ |
| Reactive Contracts 文档 | https://dev.reactive.network/education/module-1/reactive-smart-contracts |
| 主网、测试网及水龙头 | https://dev.reactive.network/reactive-mainnet |
| 官方 Ecosystem 案例 | https://reactive.network/ecosystem#cases |
| Dev 文档 Introduction | https://dev.reactive.network/education/introduction |

### 挑战任务

完成挑战：https://ethpanda.notion.site/312bbd63be878004a897e05a4841f7d4

---

## Phase 2: 理解 Reactive 技术结构与开发模型

### 学习目标

- 理解 Reactive Contract 的组成结构
- 掌握 Subscribe / Trigger / Callback 模型
- 理解 ReactVM 执行逻辑
- 理解跨链和自动化机制

### 学习材料

| 资源 | 链接 |
|------|------|
| Dev 文档核心模块 | https://dev.reactive.network/ |
| Reactive Library (核心开发库) | https://github.com/Reactive-Network/reactive-smart-contract-demos |
| Uniswap V2 止损示例 | https://github.com/Reactive-Network/reactive-smart-contract-demos/tree/main/src/demos/uniswap-v2-stop-order |
| 订阅机制 | https://dev.reactive.network/subscriptions |
| 事件与回调 | https://dev.reactive.network/events-&-callbacks |
| ReactVM 双状态模型 | https://dev.reactive.network/reactvm |
| 经济模型 | https://dev.reactive.network/economy |

### 挑战任务

完成挑战：https://ethpanda.notion.site/311bbd63be87809f9410c6fe8f8daff5?pvs=73

---

## Phase 3: 动手实践 + Casual Hackathon 准备

### 学习目标

#### 前端

- 连接钱包并切换到 Origin 链与 Lasna 链
- 实现最小交互：触发 Origin 事件
- 展示 Reactive 三段链路时间线（Origin → Reactive → Destination）

#### 后端

- 监听至少两条链，统一事件结构
- 实现推送通道（SSE 或 WebSocket）
- 调用 RNK 专用 RPC 方法进行验证
- 返回排错信息（RVM 地址、reactive 交易状态）

#### 智能合约

- 理解双状态：Reactive 合约在 Reactive Network 与私有 ReactVM 各有一份实例
- 编写 `emit Event(...)` 合约，确保事件签名（topic0）稳定
- 实现回调入口函数，第一个参数为 `address`（Destination）
- 在 `constructor` 中调用 `subscribe(chainId, originContract, topic0..topic3)` 建立订阅
- 实现 `react(LogRecord)`：从 log 读取 topics/data，做条件判断
- 在 Lasna 部署 Reactive 合约，确认系统合约地址固定为 `0x...fffFfF`

### 学习材料

| 资源 | 链接 |
|------|------|
| Dev Guide（部署与测试） | https://dev.reactive.network/ |
| 往期 Workshop | https://youtu.be/PnPIHVKPKgo?si=ENJcLHFikNB0wQK6 |
| Ecosystem 页面 | https://reactive.network/ecosystem#cases |

### 社区

- [Twitter (EN)](https://twitter.com/ReactiveNet)
- [Twitter (CN)](https://twitter.com/ReactiveNet_CN)
- [Discord](https://discord.gg/reactive)
- [Telegram](https://t.me/reactivenetwork)

---

## 学习笔记

详细学习笔记请查看：[Reactive Network × AI Agent 学习笔记.md](./Reactive%20Network%20×%20AI%20Agent%20学习笔记.md)

## License

MIT License
