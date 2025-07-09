# 🌟 Rainight - 末日生存插件

[![Minecraft](https://img.shields.io/badge/Minecraft-1.21+-green.svg)](https://minecraft.net)
[![Java](https://img.shields.io/badge/Java-21+-orange.svg)](https://openjdk.java.net)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)](target/Rainight-1.0.0.jar)

一个基于《明日之后》核心玩法设计的Minecraft 1.21生存插件，为玩家提供丰富的末日生存体验。

## 🎮 插件特色

### 🏠 庄园系统
- **建筑建造** - 住宅、生产、防御、装饰建筑
- **家具系统** - 丰富的家具装饰选择
- **庄园升级** - 扩大规模，解锁新功能
- **访客系统** - 邀请好友参观庄园

### ⚔️ 装备系统
- **装备强化** - 提升装备属性和等级
- **配件系统** - 武器配件、防具配件
- **耐久度系统** - 装备损坏和修理机制
- **装备套装** - 套装效果和属性加成

### 🎯 任务成就
- **日常任务** - 每日刷新的基础任务
- **周常任务** - 每周挑战，丰厚奖励
- **主线任务** - 推进游戏进度
- **成就系统** - 长期目标和特殊奖励

### 💰 经济系统
- **多货币系统** - 联盟币、金条、生存点数等
- **银行系统** - 存款、取款、贷款功能
- **市场交易** - 玩家间物品交易
- **税收系统** - 经济调节机制

### 👥 社交系统
- **好友系统** - 添加好友，互动交流
- **联盟系统** - 创建或加入联盟
- **排行榜** - 各种排名和竞争
- **礼品系统** - 好友间赠送礼品

### 🏕️ 营地系统
- **营地建设** - 集体建造和管理
- **防御系统** - 保护营地安全
- **资源管理** - 共享资源和分工
- **成员管理** - 营地权限和职位

### 🌡️ 环境系统
- **天气变化** - 晴天、雨天、暴风雪
- **自然灾害** - 酸雨、沙尘暴、极寒
- **环境保护** - 庄园和建筑提供保护
- **季节系统** - 不同季节的环境效果

### ❤️ 健康系统
- **营养系统** - 食物营养和健康值
- **疾病系统** - 感冒、发烧等状态
- **药品治疗** - 各种药品和治疗方法
- **锻炼系统** - 提升身体素质

## 📦 快速开始

### 系统要求
- **Minecraft**: 1.21+
- **服务端**: Leaves Server (推荐) / Paper / Spigot
- **Java**: 21+
- **内存**: 最低2GB，推荐4GB+

### 安装步骤
1. 下载 `Rainight-1.0.0.jar`
2. 将文件放入服务器的 `plugins` 文件夹
3. 重启服务器
4. 插件会自动生成配置文件和数据库

### 基础使用
```bash
# 打开主菜单 (游戏内按 R-Shift)
/rainight

# 创建庄园
/manor create 我的庄园

# 查看任务
/quest list

# 查看余额
/economy balance
```

## 🛠️ 配置文件

### 主要配置文件
- `config.yml` - 主配置文件
- `skills.yml` - 技能系统配置
- `quests.yml` - 任务系统配置
- `environment.yml` - 环境系统配置
- `health.yml` - 健康系统配置
- `equipment.yml` - 装备系统配置
- `manor.yml` - 庄园系统配置
- `camps.yml` - 营地系统配置
- `resources.yml` - 资源系统配置

### 数据库支持
- **SQLite** (默认) - 适合小型服务器
- **MySQL** - 适合大型服务器

## 📝 命令列表

### 核心命令
| 命令 | 描述 | 权限 |
|------|------|------|
| `/rainight` | 打开主菜单GUI | `rainight.use` |
| `/rainight help` | 显示帮助信息 | `rainight.use` |
| `/rainight reload` | 重载配置 | `rainight.admin` |

### 庄园命令
| 命令 | 描述 | 权限 |
|------|------|------|
| `/manor create <名称>` | 创建庄园 | `rainight.manor.create` |
| `/manor info` | 查看庄园信息 | `rainight.manor.use` |
| `/manor upgrade` | 升级庄园 | `rainight.manor.upgrade` |
| `/manor invite <玩家>` | 邀请玩家 | `rainight.manor.invite` |

### 装备命令
| 命令 | 描述 | 权限 |
|------|------|------|
| `/equipment enhance` | 强化装备 | `rainight.equipment.enhance` |
| `/equipment repair` | 修理装备 | `rainight.equipment.repair` |
| `/equipment attach <配件>` | 添加配件 | `rainight.equipment.attach` |

### 任务命令
| 命令 | 描述 | 权限 |
|------|------|------|
| `/quest list` | 查看任务列表 | `rainight.quest.use` |
| `/quest accept <ID>` | 接受任务 | `rainight.quest.accept` |
| `/quest submit <ID>` | 提交任务 | `rainight.quest.submit` |

### 经济命令
| 命令 | 描述 | 权限 |
|------|------|------|
| `/economy balance` | 查看余额 | `rainight.economy.use` |
| `/economy pay <玩家> <金额>` | 支付金钱 | `rainight.economy.pay` |
| `/market` | 打开市场 | `rainight.market.use` |

## 🎯 游戏机制

### 货币系统
- 🪙 **联盟币** - 主要货币，用于大部分交易
- 🥇 **金条** - 贵重货币，用于高级交易
- 💎 **生存点数** - 通过生存活动获得
- 🏠 **庄园币** - 庄园建设专用货币
- ⭐ **任务点数** - 完成任务获得
- 💎 **高级水晶** - 稀有货币
- 🔬 **研究代币** - 科技研究专用
- 👥 **社交信用** - 社交活动获得
- ⚡ **能量电池** - 设备运行消耗
- 🏆 **声望点数** - 声望系统货币
- 🏅 **成就勋章** - 成就系统奖励

### 技能系统
- **战斗技能** - 提升战斗能力
- **建造技能** - 提升建造效率
- **制作技能** - 提升制作成功率
- **采集技能** - 提升资源采集效率

### 等级系统
- **玩家等级** - 总体实力体现
- **庄园等级** - 庄园规模和功能
- **装备等级** - 装备强化等级
- **技能等级** - 各项技能熟练度

## 📚 文档

- [📖 玩家游玩指南](PLAYER_GUIDE.md) - 详细的游戏玩法说明
- [🛠️ 安装配置指南](INSTALLATION_GUIDE.md) - 服务器安装和配置

## 📊 项目统计

- **代码行数**: 15,000+
- **Java文件**: 119个
- **配置文件**: 10个
- **功能模块**: 8个主要模块
- **支持命令**: 50+ 个命令
- **权限节点**: 30+ 个权限

---

**🎮 开始你的末日生存之旅吧！**

在Rainight的世界中，建造你的庄园，强化你的装备，完成各种挑战，与朋友一起在末日世界中生存和发展！
