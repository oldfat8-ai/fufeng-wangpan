# fufeng-wangpan

## 项目简介

fufeng-wangpan 是一个强大的网盘资源聚合搜索平台，支持多个主流网盘的资源搜索和管理。

## 主要功能

- 多网盘资源搜索（百度网盘、夸克网盘、迅雷网盘等）
- 资源管理与统计
- 一键转存功能
- 热门资源排行
- 用户管理系统
- 操作日志记录
- 现代化的用户界面

## 技术栈

**后端**
- Go + Gin 框架
- GORM (ORM)
- MySQL 数据库
- JWT 认证

**前端**
- React 18
- TypeScript
- Ant Design
- Vite

## 快速开始

### 环境要求

- MySQL 5.7+
- Linux 服务器（支持 amd64 或 arm64 架构）

### 安装步骤

#### 1. 下载发布包

直接下载最新版本：

- Linux amd64: [点击下载](https://github.com/oldfat8-ai/fufeng-wangpan/releases/latest/download/fufeng-wangpan-v1.0.0-linux-amd64.tar.gz)
- Linux arm64: [点击下载](https://github.com/oldfat8-ai/fufeng-wangpan/releases/latest/download/fufeng-wangpan-v1.0.0-linux-arm64.tar.gz)

或前往 [Releases](https://github.com/oldfat8-ai/fufeng-wangpan/releases) 页面查看所有版本

#### 2. 解压文件

```bash
tar -xzf fufeng-wangpan-v1.0.0-linux-amd64.tar.gz
cd fufeng-wangpan-v1.0.0-linux-amd64
```

#### 3. 编辑配置文件

修改以下配置：

```yaml
database:
  host: localhost
  port: 3306
  user: root
  password: your_password
  dbname: fufeng

server:
  port: 8080
```

#### 4. 运行服务

```bash
chmod +x manager.sh
sudo ./manager.sh
```

选择 `1` 安装并启动 systemd 服务。

### 访问系统

- 前端：http://localhost:8080
- 后台：http://localhost:8080/admin
- 默认账号：`admin` / `admin123`

## 常见问题

### Q: 启动后无法访问？
A: 检查防火墙是否开放 8080 端口：
```bash
# CentOS/RHEL
sudo firewall-cmd --zone=public --add-port=8080/tcp --permanent
sudo firewall-cmd --reload

# Ubuntu/Debian
sudo ufw allow 8080
```

### Q: 数据库连接失败？
A: 检查配置文件中的数据库信息是否正确，确保 MySQL 服务已启动。

### Q: 如何修改管理员密码？
A: 登录后台后，点击右上角头像 → 修改密码。

## 联系方式

- Telegram: @xy9999bot

## 更新日志

### v1.0.0 (2026-01-17)
- 首次发布
- 支持多网盘搜索
- 用户管理系统
- 资源管理功能
- 数据统计分析
