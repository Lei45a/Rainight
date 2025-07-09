# 🛠️ Rainight插件 - 安装配置指南

## 📋 目录
- [系统要求](#系统要求)
- [安装步骤](#安装步骤)
- [配置文件](#配置文件)
- [数据库设置](#数据库设置)
- [权限配置](#权限配置)
- [故障排除](#故障排除)

---

## 💻 系统要求

### 服务器要求
- **Minecraft版本**: 1.21+
- **服务端**: Leaves Server (推荐) / Paper / Spigot
- **Java版本**: Java 21+
- **内存**: 最低2GB，推荐4GB+
- **存储**: 至少500MB可用空间

### 依赖插件
- 无硬性依赖，插件独立运行
- 可选：Vault (经济系统兼容)
- 可选：PlaceholderAPI (变量支持)

---

## 📦 安装步骤

### 1. 下载插件
- 下载 `Rainight-1.0.0.jar` 文件
- 确保文件完整，大小约为几MB

### 2. 安装插件
```bash
# 1. 停止服务器
stop

# 2. 将JAR文件放入plugins文件夹
cp Rainight-1.0.0.jar /path/to/server/plugins/

# 3. 启动服务器
start
```

### 3. 首次启动
插件首次启动时会自动：
- 创建配置文件夹 `plugins/Rainight/`
- 生成默认配置文件
- 初始化数据库
- 创建必要的数据表

### 4. 验证安装
```bash
# 在服务器控制台执行
plugins

# 应该看到 Rainight v1.0.0 [已启用]
```

---

## ⚙️ 配置文件

### 主配置文件 (config.yml)
```yaml
# 数据库配置
database:
  type: sqlite  # sqlite 或 mysql
  host: localhost
  port: 3306
  database: rainight
  username: root
  password: ""
  
# 经济系统
economy:
  enabled: true
  starting_balance: 1000
  max_balance: 999999999
  
# 庄园系统
manor:
  max_size: 100
  max_buildings: 50
  protection_enabled: true
  
# 任务系统
quests:
  daily_reset_time: "06:00"
  weekly_reset_day: "MONDAY"
  max_active_quests: 10
```

### 技能配置 (skills.yml)
```yaml
skills:
  combat:
    max_level: 100
    exp_multiplier: 1.0
  building:
    max_level: 100
    exp_multiplier: 1.0
  crafting:
    max_level: 100
    exp_multiplier: 1.0
```

### 任务配置 (quests.yml)
```yaml
daily_quests:
  kill_monsters:
    name: "击杀怪物"
    description: "击杀10只怪物"
    target: 10
    rewards:
      alliance_coins: 100
      exp: 50
      
weekly_quests:
  build_structures:
    name: "建造建筑"
    description: "建造5个建筑"
    target: 5
    rewards:
      alliance_coins: 500
      manor_coins: 200
```

### 环境配置 (environment.yml)
```yaml
weather:
  enabled: true
  change_interval: 1200  # 20分钟
  
disasters:
  acid_rain:
    enabled: true
    probability: 0.1
    duration: 300  # 5分钟
    damage: 1
    
  sandstorm:
    enabled: true
    probability: 0.05
    duration: 600  # 10分钟
```

### 健康配置 (health.yml)
```yaml
health:
  max_nutrition: 100
  max_hydration: 100
  hunger_damage: true
  thirst_damage: true
  
diseases:
  cold:
    probability: 0.02
    duration: 1200
    effects:
      - "SLOW:1"
      - "WEAKNESS:1"
```

### 装备配置 (equipment.yml)
```yaml
enhancement:
  max_level: 10
  success_rates:
    1-3: 100
    4-6: 80
    7-8: 60
    9-10: 40
    
attachments:
  weapon:
    scope: "瞄准镜"
    silencer: "消音器"
    magazine: "弹夹"
  armor:
    plate: "护甲片"
    core: "能量核心"
```

### 庄园配置 (manor.yml)
```yaml
manor:
  max_level: 50
  upgrade_costs:
    level_1: 1000
    level_2: 2000
    level_3: 5000
    
buildings:
  house:
    name: "住宅"
    max_count: 5
    build_cost: 500
  workshop:
    name: "工作坊"
    max_count: 3
    build_cost: 1000
```

### 营地配置 (camps.yml)
```yaml
camps:
  max_members: 20
  max_buildings: 30
  protection_radius: 50
  
buildings:
  wall:
    name: "围墙"
    defense: 10
    cost: 100
  tower:
    name: "箭塔"
    defense: 25
    cost: 300
```

### 资源配置 (resources.yml)
```yaml
resources:
  wood:
    name: "木材"
    rarity: common
    base_price: 10
  stone:
    name: "石材"
    rarity: common
    base_price: 15
  iron:
    name: "铁矿"
    rarity: uncommon
    base_price: 50
```

---

## 🗄️ 数据库设置

### SQLite (默认)
- 自动创建 `plugins/Rainight/database.db`
- 无需额外配置
- 适合小型服务器

### MySQL (推荐用于大型服务器)
```yaml
database:
  type: mysql
  host: localhost
  port: 3306
  database: rainight
  username: rainight_user
  password: your_password
  pool_size: 10
```

### 数据库表结构
插件会自动创建以下表：
- `player_data` - 玩家基础数据
- `manor_data` - 庄园数据
- `quest_data` - 任务数据
- `economy_data` - 经济数据
- `equipment_data` - 装备数据
- `social_data` - 社交数据

---

## 🔐 权限配置

### 基础权限
```yaml
permissions:
  rainight.use: true          # 使用插件基础功能
  rainight.gui: true          # 使用GUI界面
  rainight.manor.create: true # 创建庄园
  rainight.quest.accept: true # 接受任务
  rainight.economy.use: true  # 使用经济系统
  rainight.social.use: true   # 使用社交系统
```

### 管理员权限
```yaml
permissions:
  rainight.admin: false       # 管理员权限
  rainight.reload: false      # 重载配置
  rainight.debug: false       # 调试模式
  rainight.bypass: false      # 绕过限制
```

### 权限组示例 (LuckPerms)
```bash
# 普通玩家组
lp group default permission set rainight.use true
lp group default permission set rainight.gui true
lp group default permission set rainight.manor.create true

# VIP玩家组
lp group vip permission set rainight.manor.upgrade true
lp group vip permission set rainight.economy.bonus true

# 管理员组
lp group admin permission set rainight.admin true
lp group admin permission set rainight.reload true
```

---

## 🔧 故障排除

### 常见问题

#### 1. 插件无法启动
**症状**: 控制台显示错误信息
**解决方案**:
- 检查Java版本是否为21+
- 确认服务端版本兼容
- 查看完整错误日志

#### 2. 数据库连接失败
**症状**: 无法保存玩家数据
**解决方案**:
```bash
# 检查数据库配置
cat plugins/Rainight/config.yml

# 测试数据库连接
mysql -h localhost -u username -p database_name
```

#### 3. GUI界面无法打开
**症状**: 按R-Shift无反应
**解决方案**:
- 检查权限配置
- 确认快捷键设置
- 重启插件

#### 4. 命令无法执行
**症状**: 提示"未知命令"
**解决方案**:
```bash
# 检查插件状态
plugins

# 重载插件
rainight reload
```

#### 5. 内存不足
**症状**: 服务器卡顿或崩溃
**解决方案**:
- 增加服务器内存分配
- 优化配置文件参数
- 定期清理数据库

### 调试模式
```yaml
# 在config.yml中启用
debug:
  enabled: true
  log_level: INFO
  log_sql: false
```

### 日志文件
- 主日志: `logs/latest.log`
- 插件日志: `plugins/Rainight/logs/`
- 错误日志: `plugins/Rainight/errors.log`

### 性能优化
```yaml
# 优化配置示例
performance:
  async_saves: true
  cache_size: 1000
  cleanup_interval: 3600
  
database:
  pool_size: 5
  connection_timeout: 30
  max_lifetime: 1800
```

---

## 📞 技术支持

### 获取帮助
1. 查看日志文件确定问题
2. 检查配置文件语法
3. 确认权限设置正确
4. 联系插件开发者

### 报告Bug
提供以下信息：
- 服务器版本和插件版本
- 完整的错误日志
- 重现步骤
- 相关配置文件

### 更新插件
```bash
# 1. 备份数据
cp -r plugins/Rainight/ backup/

# 2. 停止服务器
stop

# 3. 替换JAR文件
cp Rainight-new.jar plugins/

# 4. 启动服务器
start
```

---

**安装完成后，请参考 [玩家游玩指南](PLAYER_GUIDE.md) 了解详细玩法！** 🎉
