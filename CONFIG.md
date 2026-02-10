# oll的OpenClaw工具配置

## 问题
oll只能发送消息，无法执行shell命令。

## 解决方案

在oll的OpenClaw配置文件中添加exec工具。

### 步骤1：编辑oll的配置文件

找到oll的OpenClaw配置文件（通常是 `~/.openclaw/config.yaml` 或类似位置）

### 步骤2：添加exec工具配置

```yaml
tools:
  exec:
    enabled: true
    security: allowlist  # 或 full
```

### 步骤3：重启oll的OpenClaw

```bash
openclaw restart
```

## 快速修复（临时方案）

在oll的终端直接运行：

```bash
# 测试 clawhub 是否可用
clawhub install ai-automation-workflows

# 如果oll需要独立的workspace
mkdir -p ~/.openclaw/workspace/skills
cd ~/.openclaw/workspace/skills
clawhub install ai-automation-workflows
```

## 永久解决方案

oll的OpenClaw需要在启动配置中启用exec工具。这通常在：
- 配置文件：`~/.openclaw/config.yaml`
- 环境变量：`OPENCLAW_TOOLS_EXEC_ENABLED=true`
