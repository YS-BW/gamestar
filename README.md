# 中国古代炼丹小游戏开发文档

## 项目概述

### 项目名称
暂定：**《丹道初探》**

### 主题背景
基于中国古代物理与炼丹文化，结合编程基础，设计一款以炼丹为核心玩法的小游戏。玩家通过收集材料、炼制丹药并与商人交易，体验古代炼丹的乐趣与挑战。

### 开发目标
- **截止时间**：2025年3月底或4月初（约3-4周开发周期）
- **团队规模**：3人，具备基本编程能力
- **目标平台**：PC（可选扩展至移动端）
- **核心特色**：炼丹过程的改良（火候、时长、配方）、背包管理和商人交互

---

## 核心系统设计

### 1. 背包系统
- **功能**：
  - 存储玩家收集的炼丹材料（如药草、矿石等）。
  - 存储炼制完成的丹药。
  - 显示物品名称、数量及简单描述。
- **设计要点**：
  - 网格或列表式界面，限制背包容量（例如20格）。
  - 支持物品堆叠（同类材料可叠加至一定数量，如99）。
  - 可选：物品分类（材料、丹药）。
- **实现方式**：
  - 使用数组或字典存储物品数据。
  - UI设计参考简洁的RPG游戏背包。

### 2. 炼丹系统
- **功能**：
  - 玩家选择材料，设定炼丹参数（如火候、时长），生成丹药。
  - 根据配方和参数，决定炼丹成功率及产出品质。
- **设计要点**：
  - **火候**：分为低、中、高三档，影响炼丹结果（过低失败，过高炸炉）。
  - **炼丹时长**：设定一个时间条，玩家需手动停止（类似原神烹饪的时机控制）。
  - **配方系统**：预设若干配方（例如“回气丹”需要药草x2+矿石x1），支持玩家探索隐藏配方。
  - **改良特色**：加入随机事件（如“灵气波动”增加成功率）。
- **实现方式**：
  - 使用条件判断和随机数生成炼丹结果。
  - 进度条UI模拟炼丹过程。

### 3. 商人系统
- **功能**：
  - 玩家可与商人交易，出售丹药或购买稀有材料。
- **设计要点**：
  - 商人每日刷新商品列表（随机生成）。
  - 货币系统：使用“铜钱”作为交易单位，玩家通过卖丹药或任务获取。
  - 可选：商人好感度，交易次数提升后解锁更多商品。
- **实现方式**：
  - 随机生成商品池，关联背包系统更新物品。

### 4. 日常登录系统
- **功能**：
  - 每日登录奖励玩家少量材料或铜钱。
- **设计要点**：
  - 连续登录增加奖励（如第1天1个药草，第3天5个）。
  - 可选：加入简单任务（“采集3次材料”）获取额外奖励。
- **实现方式**：
  - 本地存储记录登录时间和奖励状态。

### 5. 其他系统（可选）
- **简单剧情**：玩家扮演初学者，逐步解锁更高级炼丹术。
- **音效与美术**：加入炼丹炉火声、中国风背景音乐，简笔画风格素材。

---

## 技术选型

### 开发工具
- **游戏引擎**：
  - **Unity**：支持2D开发，易于上手，适合快速原型。
- **编程语言**：
  - Unity使用C#。
- **美术资源**：
  - 使用免费素材网站（如OpenGameArt）或简单手绘。
- **音效资源**：
  - Freesound.org提供免费音效。

### 团队分工建议
- **成员1**：负责背包系统和UI设计。
- **成员2**：负责炼丹系统核心逻辑。
- **成员3**：负责商人系统、日常登录系统及整合。

---

## 开发计划

### 时间表（3-4周）
- **第1周（3月6日-3月12日）**：
  - 确定技术选型，搭建基本项目框架。
  - 设计游戏核心玩法（炼丹逻辑、背包原型）。
- **第2周（3月13日-3月19日）**：
  - 完成背包系统和炼丹系统初版。
  - 开始商人系统开发。
- **第3周（3月20日-3月26日）**：
  - 完善商人系统和日常登录系统。
  - 进行UI优化，添加音效和简单美术。
- **第4周（3月27日-4月2日）**：
  - 测试与调试，修复bug。
  - 准备大赛提交（文档、演示视频）。

### 里程碑
1. **基础框架完成**：第1周末。
2. **核心玩法可玩**：第2周末。
3. **完整游戏初版**：第3周末。
4. **最终提交版本**：4月2日。

---

## 注意事项

1. **时间管理**：
   - 优先完成核心系统（背包+炼丹），其他功能视时间调整。
2. **技术难度**：
   - 避免过于复杂的算法，保持简单可实现。
3. **主题契合**：
   - 强调中国古代炼丹特色（如加入“五行”元素）。
4. **团队协作**：
   - 使用GitHub进行代码管理，每日更新进度。
## 相关链接
   - https://developer.unity.cn/projects/5e5a6348edbc2a2fcabae21b 【UnityTips】一种仿 Minecraft 物品合成的思路
---

## 初期任务清单
- [ ] 下载并学习Unity基础教程（1-2天）。
- [ ] 设计炼丹配方表（至少5种丹药）。
- [ ] 绘制简单游戏流程图。
- [ ] 分配具体开发任务。


