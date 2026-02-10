# oll-config

oll的OpenClaw配置文件仓库。

## 使用方法

1. 克隆到oll的workspace目录：
   ```bash
   git clone https://github.com/你的用户名/oll-config.git ~/.openclaw/workspace
   ```

2. 或者只克隆配置文件：
   ```bash
   git init
   git remote add origin https://github.com/你的用户名/oll-config.git
   git pull origin main
   ```

## 文件说明

- `SOUL.md` - oll的身份设定
- `USER.md` - 用户信息
- `AGENTS.md` - 工作空间配置和工具说明

## 更新配置

当需要更新oll的配置时：
1. 在此仓库修改文件
2. 提交并推送
3. oll执行 `git pull` 更新
