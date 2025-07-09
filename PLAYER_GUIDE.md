# 🌟 Rainight插件 - 玩家游玩指南

## 📋 目录
- [插件介绍](#插件介绍)
- [快速开始](#快速开始)
- [核心系统](#核心系统)
- [命令大全](#命令大全)
- [游戏机制](#游戏机制)
- [进阶玩法](#进阶玩法)

---

## 🎮 插件介绍

**Rainight** 是一个基于《明日之后》核心玩法设计的Minecraft 1.21生存插件，提供了丰富的末日生存体验：

### ✨ 核心特色
- 🏠 **庄园系统** - 建造和管理你的专属庄园
- ⚔️ **装备强化** - 装备配件、强化、修理系统
- 🎯 **任务成就** - 丰富的日常、周常任务和成就系统
- 💰 **经济系统** - 多货币、银行、市场交易
- 👥 **社交系统** - 好友、联盟、排行榜
- 🏕️ **营地系统** - 建设和防御营地
- 🌡️ **环境系统** - 天气、灾害、环境效果
- ❤️ **健康系统** - 营养、疾病、状态管理

---

## 🚀 快速开始

### 第一次进入游戏

1. **打开主菜单**
   ```
   按 R-Shift 键打开主GUI界面
   ```

2. **查看个人状态**
   ```
   /rainight health - 查看健康状态
   /rainight inventory - 查看背包信息
   ```

3. **创建庄园**
   ```
   /manor create <庄园名称> - 创建你的第一个庄园
   ```

### 基础操作
- **R-Shift** - 打开主菜单GUI
- **主菜单包含**：健康、装备、庄园、任务、市场、社交、设置等

---

## 🏗️ 核心系统

### 🏠 庄园系统
庄园是你的专属基地，可以建造建筑、放置家具、邀请好友参观。

**基础操作：**
- `/manor create <名称>` - 创建庄园
- `/manor info` - 查看庄园信息
- `/manor upgrade` - 升级庄园
- `/manor invite <玩家>` - 邀请玩家参观

**建筑系统：**
- 住宅建筑：提供休息和存储功能
- 生产建筑：制作物品和资源
- 防御建筑：保护庄园安全
- 装饰建筑：美化庄园环境

### ⚔️ 装备系统
强化你的装备，添加配件，提升战斗力。

**装备强化：**
- `/equipment enhance` - 强化装备
- `/equipment repair` - 修理装备
- `/equipment attach` - 添加配件

**配件系统：**
- 武器配件：瞄准镜、消音器、弹夹等
- 防具配件：护甲片、能量核心等

### 🎯 任务系统
完成各种任务获得奖励和经验。

**任务类型：**
- **日常任务** - 每日刷新，基础奖励
- **周常任务** - 每周刷新，丰厚奖励
- **主线任务** - 推进游戏进度
- **成就系统** - 长期目标挑战

**任务操作：**
- `/quest list` - 查看任务列表
- `/quest accept <任务ID>` - 接受任务
- `/quest submit <任务ID>` - 提交任务
- `/quest abandon <任务ID>` - 放弃任务

### 💰 经济系统
多种货币系统，支持交易和投资。

**货币类型：**
- 🪙 **联盟币** - 主要货币
- 🥇 **金条** - 贵重货币
- 💎 **生存点数** - 生存活动获得
- 🏠 **庄园币** - 庄园建设专用
- ⭐ **任务点数** - 完成任务获得

**经济操作：**
- `/economy balance` - 查看余额
- `/economy transfer <玩家> <金额> <货币>` - 转账
- `/economy bank` - 银行操作
- `/market` - 打开市场

### 👥 社交系统
与其他玩家互动，建立联盟。

**好友系统：**
- `/social friend add <玩家>` - 添加好友
- `/social friend list` - 好友列表
- `/social friend remove <玩家>` - 删除好友

**联盟系统：**
- `/social alliance create <名称>` - 创建联盟
- `/social alliance join <联盟>` - 加入联盟
- `/social alliance leave` - 离开联盟

---

## 📝 命令大全

### 🎮 主要命令

#### 核心命令
```bash
/rainight                    # 打开主菜单GUI
/rainight help              # 显示帮助信息
/rainight reload            # 重载插件配置
```

#### 庄园命令
```bash
/manor create <名称>         # 创建庄园
/manor delete               # 删除庄园
/manor info                 # 庄园信息
/manor upgrade              # 升级庄园
/manor invite <玩家>        # 邀请参观
/manor kick <玩家>          # 踢出访客
/manor settings             # 庄园设置
/manor build <建筑类型>     # 建造建筑
/manor furniture <家具>     # 放置家具
```

#### 装备命令
```bash
/equipment info             # 装备信息
/equipment enhance          # 强化装备
/equipment repair           # 修理装备
/equipment attach <配件>    # 添加配件
/equipment detach <配件>    # 移除配件
/equipment upgrade          # 升级装备
```

#### 任务命令
```bash
/quest list                 # 任务列表
/quest daily                # 日常任务
/quest weekly               # 周常任务
/quest accept <ID>          # 接受任务
/quest submit <ID>          # 提交任务
/quest abandon <ID>         # 放弃任务
/quest progress <ID>        # 任务进度
```

#### 经济命令
```bash
/economy balance            # 查看余额
/economy pay <玩家> <金额>  # 支付
/economy transfer <玩家> <金额> <货币> # 转账
/economy history            # 交易历史
/economy bank deposit <金额> # 银行存款
/economy bank withdraw <金额> # 银行取款
/economy bank loan <金额>   # 申请贷款
```

#### 市场命令
```bash
/market                     # 打开市场GUI
/market sell <物品> <价格>  # 出售物品
/market buy <ID>            # 购买物品
/market list                # 市场列表
/market search <关键词>     # 搜索物品
```

#### 社交命令
```bash
/social friend add <玩家>   # 添加好友
/social friend remove <玩家> # 删除好友
/social friend list         # 好友列表
/social alliance create <名称> # 创建联盟
/social alliance join <联盟> # 加入联盟
/social alliance leave      # 离开联盟
/social alliance info       # 联盟信息
/social leaderboard         # 排行榜
```

#### 营地命令
```bash
/camp create <名称>         # 创建营地
/camp join <营地>           # 加入营地
/camp leave                 # 离开营地
/camp info                  # 营地信息
/camp build <建筑>          # 建造建筑
/camp defend                # 防御设置
```

#### 健康命令
```bash
/health status              # 健康状态
/health eat <食物>          # 食用食物
/health drink <饮品>        # 饮用饮品
/health medicine <药品>     # 使用药品
/health exercise            # 锻炼身体
```

#### 技能命令
```bash
/skill list                 # 技能列表
/skill info <技能>          # 技能信息
/skill upgrade <技能>       # 升级技能
/skill reset                # 重置技能点
```

#### 背包命令
```bash
/inventory info             # 背包信息
/inventory sort             # 整理背包
/inventory expand           # 扩展背包
/inventory search <物品>    # 搜索物品
```

#### 制作命令
```bash
/craft list                 # 制作列表
/craft recipe <物品>        # 查看配方
/craft make <物品> [数量]   # 制作物品
/craft queue                # 制作队列
```

#### 设置命令
```bash
/settings                   # 打开设置GUI
/settings language <语言>   # 设置语言
/settings notification <开关> # 通知设置
/settings privacy <级别>    # 隐私设置
```

---

## 🎯 游戏机制

### 💪 健康系统
- **营养值**：影响生命恢复和状态
- **水分值**：影响移动速度和耐力
- **疾病系统**：感冒、发烧等状态效果
- **药品治疗**：使用药品恢复健康

### 🌡️ 环境系统
- **天气变化**：晴天、雨天、暴风雪
- **自然灾害**：酸雨、沙尘暴、极寒
- **环境保护**：庄园可提供环境保护

### 🔧 制作系统
- **工作台制作**：基础物品制作
- **专业设备**：高级物品需要专业设备
- **材料收集**：从环境中收集制作材料

### 📈 经验系统
- **技能经验**：通过使用技能获得经验
- **任务经验**：完成任务获得大量经验
- **庄园经验**：建设庄园获得经验

---

## 🏆 进阶玩法

### 🏰 庄园建设
1. **规划布局** - 合理安排建筑位置
2. **资源管理** - 平衡生产和消耗
3. **防御建设** - 保护庄园免受攻击
4. **美化装饰** - 提升庄园等级和美观度

### ⚔️ PvP战斗
1. **装备强化** - 提升装备属性
2. **技能搭配** - 选择合适的技能组合
3. **战术运用** - 利用地形和环境优势
4. **团队协作** - 与联盟成员配合作战

### 💼 商业经营
1. **市场分析** - 了解物品价格趋势
2. **投资理财** - 银行存款和贷款
3. **贸易路线** - 建立稳定的交易关系
4. **垄断经营** - 控制特定物品市场

### 🤝 社交网络
1. **好友互助** - 互相帮助完成任务
2. **联盟建设** - 建立强大的联盟
3. **外交关系** - 与其他联盟建立关系
4. **声望系统** - 提升个人和联盟声望

---

## 🎮 游戏小贴士

### 💡 新手建议
- 优先完成日常任务获得基础资源
- 尽早创建庄园开始建设
- 加入活跃的联盟获得帮助
- 合理分配技能点数

### 🔥 高效玩法
- 每日登录完成日常任务
- 参与联盟活动获得额外奖励
- 关注市场价格进行交易
- 定期强化和修理装备

### ⚠️ 注意事项
- 注意健康值，及时补充营养
- 关注天气变化，做好防护
- 定期备份重要物品
- 遵守服务器规则

---

## 📞 联系支持

如果在游戏过程中遇到问题，可以：
- 使用 `/rainight help` 查看帮助
- 联系服务器管理员
- 查看插件官方文档

---

**祝您在Rainight的世界中玩得愉快！** 🎉
