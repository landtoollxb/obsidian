# Android 同步（HTTPS + PAT）

## 0. 先说明
- 移动端 Obsidian Git 通常不支持 SSH
- Android 端建议使用 HTTPS + GitHub Token（PAT）
- 仓库地址：`https://github.com/landtoollxb/obsidian.git`

## 1. 在 GitHub 创建 PAT（Fine-grained token）
- GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens
- Repository access：只选择 `landtoollxb/obsidian`
- Permissions（最小权限，按界面为准）：
  - Contents：Read and write
  - Metadata：Read

## 2. Android 安装 Obsidian 并准备 Vault
- 安装 Obsidian（Android）
- 创建一个空目录（建议）：`/storage/emulated/0/Documents/ObsidianVault`
- 用 Obsidian 打开这个目录作为 Vault

## 3. 安装 Obsidian Git 插件
- Settings → Community plugins
  - 关闭 Safe mode
  - Browse → 安装 Obsidian Git

## 4. 配置认证（HTTPS + PAT）
- Settings → Obsidian Git
  - Username：`landtoollxb`
  - Password/Token：填刚创建的 PAT

## 5. 克隆仓库
- 打开命令面板（Command palette）
- 运行：Git: Clone existing remote repo
- URL：`https://github.com/landtoollxb/obsidian.git`
- 目标目录选择你刚创建的空 Vault 目录

## 6. 同步习惯（推荐）
- 启动后先 Pull
- 编辑结束后手动 Commit-and-sync
- 移动端尽量不要同时与电脑端编辑同一篇笔记，冲突优先在电脑处理

