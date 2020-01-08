# 部署

## 开始部署

- `docker-compose build`
- `docker-compose up -d`

## 移除部署

- `docker-compose stop`
- `docker-compose rm`

## 查看启动错误日志

- `docker-compose logs`

## nginx 常见错误

- while connecting to upstream, client: 172.18.0.1, server: localhost
- 解决方案 使用本机真实 IP 地址
- 解决方案
  - `setsebool -P httpd_can_network_connect 1`
  - `打开 vim /etc/selinux/config 找到 SELINUX=enforcing 改为 SELINUX=disabled`
