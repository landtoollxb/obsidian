---
type: home
topic: ubuntu
---

# Ubuntu 命令速查入口（24.04）

适用场景：Ubuntu 24.04 日常运维 + 大数据平台部署前置（SSH/网络/磁盘/systemd/日志/限制项）。

## 速查
- [[05-KB/Ubuntu/Linux-Commands/00-总览速查|00-总览速查]]
- [[05-KB/Ubuntu/Linux-Commands/20-大数据部署前置|20-大数据部署前置]]

## 分类
- [[05-KB/Ubuntu/Linux-Commands/01-文件与目录|01-文件与目录]]
- [[05-KB/Ubuntu/Linux-Commands/02-文本处理与检索|02-文本处理与检索]]
- [[05-KB/Ubuntu/Linux-Commands/03-权限与用户|03-权限与用户]]
- [[05-KB/Ubuntu/Linux-Commands/04-进程与服务-systemd|04-进程与服务-systemd]]
- [[05-KB/Ubuntu/Linux-Commands/05-网络与远程|05-网络与远程]]
- [[05-KB/Ubuntu/Linux-Commands/06-磁盘与存储|06-磁盘与存储]]
- [[05-KB/Ubuntu/Linux-Commands/07-包管理与软件|07-包管理与软件]]
- [[05-KB/Ubuntu/Linux-Commands/08-安全与防火墙|08-安全与防火墙]]
- [[05-KB/Ubuntu/Linux-Commands/09-定时任务|09-定时任务]]
- [[05-KB/Ubuntu/Linux-Commands/10-性能与排障|10-性能与排障]]

## 学习路径（建议）
1. 先熟悉：文件/文本/权限（01/02/03）
2. 再掌握：systemd + journalctl（04）
3. 部署必备：网络/SSH/端口/解析（05）
4. 大数据落地：磁盘挂载 + limits + sysctl + 时间同步（06 + 20）

## 快速索引（Dataview）
```dataview
TABLE file.mtime AS 更新
FROM "05-KB/Ubuntu/Linux-Commands"
SORT file.name ASC
```

