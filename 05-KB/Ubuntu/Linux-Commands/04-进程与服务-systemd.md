---
type: handbook
topic: systemd
os: ubuntu
---

# 进程与服务（systemd）

## 进程查看
```bash
ps aux | head
ps -ef | grep java
ps -eo pid,ppid,user,%cpu,%mem,cmd --sort=-%cpu | head
pgrep -a java
```

## 资源监控
```bash
top
free -h
uptime
```

可选工具：
```bash
sudo apt update
sudo apt install -y htop
htop
```

## kill（优先温和）
```bash
kill -15 PID
kill -9 PID
pkill -f "kafka.Kafka"
```

## systemctl（服务管理）
```bash
systemctl status ssh -l
sudo systemctl start ssh
sudo systemctl stop ssh
sudo systemctl restart ssh
sudo systemctl enable ssh
sudo systemctl disable ssh
systemctl list-units --type=service --state=running
```

## journalctl（日志）
```bash
journalctl -u ssh -e
journalctl -u ssh -n 200
journalctl -u ssh -f
journalctl -p err -b
```

## 写一个最小 systemd 服务（部署常用）
示例：把应用当作服务托管（按需修改路径/用户/命令）

文件：`/etc/systemd/system/myapp.service`
```ini
[Unit]
Description=My App
After=network.target

[Service]
Type=simple
User=hadoop
WorkingDirectory=/data/myapp
ExecStart=/data/myapp/bin/start.sh
Restart=on-failure
RestartSec=5
LimitNOFILE=65535

[Install]
WantedBy=multi-user.target
```

启用：
```bash
sudo systemctl daemon-reload
sudo systemctl enable --now myapp
systemctl status myapp -l
journalctl -u myapp -f
```

## 常见坑
- 改了 service 文件必须 `daemon-reload`。
- 排障优先看 `systemctl status -l` 和 `journalctl -u xxx -e`。

