# Windows 插件配置

## 1. 开启社区插件
- Settings → Community plugins
- 关闭 Safe mode

## 2. 安装插件（按顺序）
1) Git（Obsidian Git / obsidian-git）  
2) Templater  
3) Calendar  
4) Dataview  
5) QuickAdd  

### 2.1 如果在市场里搜不到 Git（Obsidian Git）
- 确认：Community plugins 已关闭 Safe mode
- 在 Browse 里用关键词 `Git` 搜索，不要用 `Obsidian Git`
- 避免装错：GitHobs 不是用于仓库同步的插件

### 2.2 手动安装 Git（Obsidian Git）
- 下载 `obsidian-git-<版本号>.zip`（来自 Vinzent03/obsidian-git 的 Releases）
- 解压到：`E:\obsidian\ObsidianVault\.obsidian\plugins\obsidian-git\`
- 重启 Obsidian → Settings → Community plugins → 启用 Git

## 3. Templater
- Settings → Templater
- Template folder location：`99-Templates`

## 4. Daily Notes（核心插件）
- Settings → Core plugins → 启用 Daily notes
- Settings → Daily notes
  - New file location：`01-Daily`
  - Template file location：`99-Templates/Daily.md`
  - Date format：`YYYY-MM-DD`

## 5. Calendar
- Settings → Community plugins → Calendar
- 打开 Calendar 视图后，点击日期会创建/打开对应日记

## 6. Dataview
- Settings → Dataview
  - Enable JavaScript queries：关闭（先保持更安全、更稳定）
- 打开 [主页](file:///E:/obsidian/ObsidianVault/90-Home/%E4%B8%BB%E9%A1%B5.md)

## 7. QuickAdd（建议做 3 个 Capture）
### 7.1 Capture：Inbox
- Capture to file：`00-Inbox/{{DATE:YYYY-MM-DD}}-{{TIME:HHmm}}.md`
- Template：`99-Templates/Capture-Inbox.md`

### 7.2 Capture：读书笔记
- Capture to file：`03-Reading/{{VALUE:书名}}.md`
- Template：`99-Templates/Reading.md`

### 7.3 Capture：代码笔记
- Capture to file：`04-DevNotes/{{VALUE:标题}}.md`
- Template：`99-Templates/DevNote.md`

## 8. Obsidian Git（电脑端）
### 8.1 推荐设置
- Pull on startup：开启
- Pull before push：开启
- Auto backup：建议先关闭或设为 10–30 分钟，稳定后再调小

### 8.2 推荐使用方式
- 开始编辑前：Pull
- 结束编辑后：Commit-and-sync
