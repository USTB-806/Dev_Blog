---
title: "Linux 使用 V2ray 补充"
date: 2025-11-04
draft: false
---

参考[Linux下V2Ray安装配置指南](https://jishuzhan.net/article/1932679439594336257)完成 V2ray 配置后，继续添加以下步骤方便服务器所有y应用走代理。

## 设置系统级代理

创建系统级环境变量文件：

```bash
sudo vim /etc/profile.d/proxy.sh
```

将以下内容添加到文件中

```bash
# 系统级代理设置
export http_proxy=http://127.0.0.1:10809
export https_proxy=http://127.0.0.1:10809
export HTTP_PROXY=http://127.0.0.1:10809
export HTTPS_PROXY=http://127.0.0.1:10809
```

保存并退出，设置文件权限

```bash
sudo chmod 644 /etc/profile.d/proxy.sh
```

让任意普通用户执行以下命令验证是否生效：

```bash
# 新开一个终端或重新登录后执行
echo $http_proxy
echo $https_proxy
```

如果输出显示 `http://127.0.0.1:10809`，则说明配置成功。

## 为所有用户添加代理开关功能

创建系统级别的别名：

```bash
sudo vim /etc/profile.d/proxy-alias.sh
```

```bash
# 系统级代理开关命令
alias proxy-on='export http_proxy=http://127.0.0.1:10809; export https_proxy=http://127.0.0.1:10809; export HTTP_PROXY=http://127.0.0.1:10809; export HTTPS_PROXY=http://127.0.0.1:10809; echo "✓ 代理已开启"'
alias proxy-off='unset http_proxy https_proxy HTTP_PROXY HTTPS_PROXY; echo "✗ 代理已关闭"'
alias proxy-status='if [ -n "$http_proxy" ]; then echo "代理状态: 已开启"; echo "HTTP代理: $http_proxy"; echo "HTTPS代理: $https_proxy"; else echo "代理状态: 已关闭"; fi'
```

保存并设置权限：
```bash
sudo chmod 644 /etc/profile.d/proxy-alias.sh
```

添加以下内容：

```bash
# 系统级代理开关命令
alias proxy-on='export http_proxy=http://127.0.0.1:10809; export https_proxy=http://127.0.0.1:10809; export HTTP_PROXY=http://127.0.0.1:10809; export HTTPS_PROXY=http://127.0.0.1:10809; echo "✓ 代理已开启"'
alias proxy-off='unset http_proxy https_proxy HTTP_PROXY HTTPS_PROXY; echo "✗ 代理已关闭"'
alias proxy-status='if [ -n "$http_proxy" ]; then echo "代理状态: 已开启"; echo "HTTP代理: $http_proxy"; echo "HTTPS代理: $https_proxy"; else echo "代理状态: 已关闭"; fi'
```

保存并设置权限：

```bash
sudo chmod 644 /etc/profile.d/proxy-alias.sh
```

## motd 提示代理状态

为了让用户知道服务器已经配置了代理以及使用方法，可以在登录时显示相关提示信息。

编辑 `/etc/motd` 文件：

```bash
sudo vim /etc/motd
```

添加以下内容：

```bash
# 系统代理状态提示
已配置 v2ray，使用 proxy-on 开启代理，proxy-off 关闭代理，proxy-status 查看代理状态；
配置文件位于 /usr/local/etc/v2ray/config.json

测试Google连接命令：
curl -v https://www.google.com
```