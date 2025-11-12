---
title: "开发运维"
date: 2025-11-12
draft: false
---
![beautiful_pic](/images/devops.jpg)
运行维护是开发者在部署、维护和扩展应用程序时需要掌握的知识和工具。

## Docker

Docker 是一个开源的容器化平台，用于开发、交付和运行应用程序。通过容器化，你可以将应用程序及其依赖打包成一个轻量级的、可移植的容器，确保在任何环境中一致运行。

Docker 的核心概念包括镜像（Image）、容器（Container）、Dockerfile 和 Docker Compose。镜像是一个只读模板，用于创建容器；容器是镜像的运行实例。

[访问官网](https://www.docker.com/) 了解更多。欲了解更多关于 Docker 的内容，请自行探索。

### Checklist

下面给出一个 Docker 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我安装了 Docker，并且知道如何运行一个简单的容器（如 hello-world）。
- [ ] 我知道如何使用 Dockerfile 构建一个自定义镜像。
- [ ] 我能使用 Docker Compose 来运行多容器应用程序。

**基础级：**

- [ ] 我知道如何管理容器生命周期（启动、停止、删除）。
- [ ] 我了解 Docker 网络和卷（Volumes）的概念，并能配置它们。
- [ ] 我知道如何推送和拉取镜像到 Docker Hub 或私有仓库。

**进阶级：**

- [ ] 我知道如何优化 Dockerfile 以减少镜像大小。
- [ ] 我了解 Docker Swarm 或 Kubernetes 的基本概念，并能部署简单的集群。
- [ ] 我知道如何在生产环境中使用 Docker，包括安全和监控。

## CI/CD

持续集成（CI）和持续交付/部署（CD）是现代软件开发中的关键实践。CI/CD 自动化了代码集成、测试和部署过程，帮助团队更快、更可靠地交付软件。

常见的 CI/CD 工具包括 GitHub Actions、Jenkins、GitLab CI/CD 等。这些工具允许你定义流水线（Pipelines），自动运行测试、构建和部署。

[访问 GitHub Actions 文档](https://docs.github.com/en/actions) 了解更多。欲了解更多关于 CI/CD 的内容，请自行探索。

### Checklist

下面给出一个 CI/CD 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道 CI/CD 的基本概念，并能解释为什么它重要。
- [ ] 我使用过至少一种 CI/CD 工具（如 GitHub Actions），并能创建一个简单的流水线。
- [ ] 我知道如何在流水线中运行自动化测试。

**基础级：**

- [ ] 我能配置多阶段流水线，包括构建、测试和部署阶段。
- [ ] 我了解环境变量和秘密（Secrets）的管理。
- [ ] 我知道如何处理流水线失败和回滚。

**进阶级：**

- [ ] 我能优化流水线性能，如并行执行和缓存。
- [ ] 我了解蓝绿部署和金丝雀部署等高级部署策略。
- [ ] 我知道如何集成监控和日志记录到 CI/CD 流程中。

## GitHub Pages 部署

GitHub Pages 是 GitHub 提供的免费静态网站托管服务，非常适合部署个人博客、项目文档、作品集等静态网站。结合 GitHub Actions，你可以实现自动化构建和部署工作流。

GitHub Pages 支持直接从仓库部署静态文件，也支持 Jekyll 等静态站点生成器。你可以使用自定义域名，并且 GitHub 会自动提供 HTTPS 支持。通过 GitHub Actions 工作流，每次推送代码时可以自动构建并部署网站。

[访问 GitHub Pages 文档](https://docs.github.com/en/pages) 了解更多。

### Checklist

下面给出一个 GitHub Pages 部署掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我了解 GitHub Pages 的基本概念和使用场景。
- [ ] 我能从仓库的特定分支（如 main 或 gh-pages）部署静态网站。
- [ ] 我知道如何在仓库设置中配置 GitHub Pages。

**基础级：**

- [ ] 我能编写 GitHub Actions 工作流自动化部署静态网站。
- [ ] 我了解如何配置自定义域名和 CNAME 记录。
- [ ] 我知道如何使用 Jekyll、Hugo 或其他静态站点生成器。

**进阶级：**

- [ ] 我能配置复杂的构建流程（如 npm build、多步骤构建）。
- [ ] 我了解如何使用 GitHub Actions 缓存来加速构建。
- [ ] 我能处理部署失败、回滚和多环境部署。
- [ ] 我知道如何优化网站性能和 SEO。

## Linux

Linux 是一个开源的操作系统内核，许多服务器和嵌入式系统都基于它。掌握 Linux 是运行维护的基础，因为大多数生产环境运行在 Linux 上。

Linux 提供了强大的命令行工具、文件系统管理和进程控制。常见的发行版包括 Ubuntu、CentOS、Debian 等。

欲了解更多关于 Linux 的内容，请自行探索。

### Checklist

下面给出一个 Linux 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道如何在 Linux 系统上导航文件系统（ls、cd、pwd）。
- [ ] 我能使用基本命令管理文件（cp、mv、rm、mkdir）。
- [ ] 我知道如何查看系统信息（如 uname、df、free）。

**基础级：**

- [ ] 我了解用户和权限管理（useradd、chmod、chown）。
- [ ] 我能安装和管理软件包（apt、yum、dnf）。
- [ ] 我知道如何监控系统资源和进程（top、ps、kill）。

**进阶级：**

- [ ] 我能编写简单的 Shell 脚本自动化任务。
- [ ] 我了解网络配置和防火墙（iptables、ufw）。
- [ ] 我知道如何设置和维护服务器，包括日志管理和备份。

## Shell 脚本

Shell 脚本是自动化运维任务的核心技能。通过编写 Shell 脚本，你可以自动化重复性任务，如系统监控、日志分析、备份等。

常用的 Shell 包括 Bash、Zsh 等。Shell 脚本支持变量、条件判断、循环、函数等编程特性，可以调用系统命令完成复杂的运维操作。

### Checklist

下面给出一个 Shell 脚本掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我能编写简单的 Shell 脚本并使其可执行（chmod +x）。
- [ ] 我了解变量、字符串操作和基本的输入输出。
- [ ] 我能使用条件判断（if-else）和循环（for、while）。

**基础级：**

- [ ] 我能编写脚本分析服务器性能统计（CPU、内存、磁盘使用率）。
- [ ] 我了解如何处理命令行参数和选项。
- [ ] 我能使用管道、重定向和文本处理工具（grep、awk、sed）。

**进阶级：**

- [ ] 我能编写复杂的日志分析脚本。
- [ ] 我了解错误处理和调试技巧（set -e、trap）。
- [ ] 我能编写可维护、可重用的脚本库。

## Systemd

Systemd 是现代 Linux 发行版的系统和服务管理器，用于启动、停止和管理系统服务。它提供了并行启动、按需激活和依赖管理等特性。

通过 Systemd，你可以创建自定义服务单元（Service Units），管理服务的生命周期，设置自动重启策略，以及查看服务日志。

### Checklist

下面给出一个 Systemd 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道如何使用 systemctl 命令管理服务（start、stop、restart、status）。
- [ ] 我能查看服务日志（journalctl）。
- [ ] 我了解如何设置服务开机自启（enable、disable）。

**基础级：**

- [ ] 我能创建一个简单的 systemd 服务单元文件。
- [ ] 我了解服务单元的基本配置（Type、ExecStart、Restart）。
- [ ] 我知道如何配置服务依赖关系（After、Requires）。

**进阶级：**

- [ ] 我能配置复杂的服务单元，包括环境变量、工作目录等。
- [ ] 我了解不同的服务类型（simple、forking、oneshot、notify）。
- [ ] 我能使用 systemd 定时器（Timers）替代 cron。

## Caddy/Nginx

Caddy 和 Nginx 是流行的 Web 服务器和反向代理服务器，用于处理 HTTP 请求、负载均衡和 SSL 证书管理。

Nginx 以高性能和稳定性著称，而 Caddy 以自动 HTTPS 和简单配置闻名。它们常用于部署 Web 应用程序、API 和静态站点。

[访问 Nginx 官网](https://nginx.org/) 和 [Caddy 官网](https://caddyserver.com/) 了解更多。欲了解更多关于反向代理的内容，请自行探索。

### Checklist

下面给出一个 Caddy/Nginx 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道如何安装和启动 Nginx 或 Caddy。
- [ ] 我能配置一个简单的静态站点服务。
- [ ] 我了解反向代理的基本概念，并能设置一个简单的代理。

**基础级：**

- [ ] 我能配置 SSL 证书（Nginx 使用 Let's Encrypt，Caddy 自动）。
- [ ] 我知道如何设置负载均衡和缓存。
- [ ] 我能处理常见的配置问题，如重定向和错误页面。

**进阶级：**

- [ ] 我能优化服务器性能，包括压缩和调优。
- [ ] 我了解高级功能，如 WebSocket 支持和限流。
- [ ] 我知道如何监控和日志记录服务器活动。

## Kubernetes

Kubernetes（简称 K8s）是一个开源的容器编排平台，用于自动化部署、扩展和管理容器化应用程序。它提供了强大的功能，如服务发现、负载均衡、自动扩展和自我修复。

Kubernetes 使用 Pod、Service、Deployment 等概念来管理容器。常见的工具包括 kubectl 命令行工具和 Helm 包管理器。

[访问官网](https://kubernetes.io/) 了解更多。欲了解更多关于 Kubernetes 的内容，请自行探索。

### Checklist

下面给出一个 Kubernetes 掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道 Kubernetes 的基本概念，如 Pod、Node 和 Cluster。
- [ ] 我安装了 kubectl，并能连接到一个 Kubernetes 集群。
- [ ] 我能使用 kubectl 部署一个简单的应用程序。

**基础级：**

- [ ] 我了解 Service 和 Ingress 的概念，并能配置它们。
- [ ] 我知道如何使用 ConfigMap 和 Secret 管理配置。
- [ ] 我能监控 Pod 的状态和日志。

**进阶级：**

- [ ] 我了解 Helm 的使用，并能部署复杂的应用程序。
- [ ] 我知道如何设置自动扩展（HPA）和滚动更新。
- [ ] 我能排查 Kubernetes 集群中的常见问题。

## 监控和日志

监控和日志记录是运行维护中的重要组成部分，帮助你跟踪应用程序性能、检测问题并进行故障排除。

常见的工具包括 Prometheus（用于指标收集）、Grafana（用于可视化）、ELK Stack（Elasticsearch、Logstash、Kibana，用于日志管理）。

[访问 Prometheus 官网](https://prometheus.io/) 和 [Grafana 官网](https://grafana.com/) 了解更多。欲了解更多关于监控和日志的内容，请自行探索。

### Checklist

下面给出一个监控和日志掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道监控和日志的基本概念，并能解释为什么它们重要。
- [ ] 我使用过至少一种监控工具（如 Prometheus），并能收集基本指标。
- [ ] 我知道如何查看应用程序日志。

**基础级：**

- [ ] 我能配置告警规则和通知。
- [ ] 我了解日志聚合和搜索（如使用 ELK）。
- [ ] 我知道如何使用 Grafana 创建仪表板。

**进阶级：**

- [ ] 我能优化监控配置以减少开销。
- [ ] 我了解分布式跟踪和 APM（Application Performance Monitoring）。
- [ ] 我知道如何分析日志以进行根因分析。

## 安全

安全是运行维护中的关键方面，包括保护应用程序、数据和基础设施免受威胁。

常见的安全实践包括使用防火墙、SSL/TLS 加密、访问控制和定期更新。工具如 fail2ban（防止暴力破解）和 Let's Encrypt（免费 SSL 证书）。

欲了解更多关于安全的内容，请自行探索。

### Checklist

下面给出一个安全掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道基本的安全概念，如加密和认证。
- [ ] 我能配置防火墙（如 ufw 或 iptables）。
- [ ] 我知道如何使用 SSL/TLS 保护通信。

**基础级：**

- [ ] 我了解访问控制和最小权限原则。
- [ ] 我能定期更新系统和软件以修补漏洞。
- [ ] 我知道如何监控安全事件和日志。

**进阶级：**

- [ ] 我了解容器安全和镜像扫描。
- [ ] 我知道如何实施零信任架构。
- [ ] 我能进行渗透测试和漏洞评估。

## 云服务基础

云服务提供了可扩展的计算资源，帮助开发者快速部署和管理应用程序。主要的云提供商包括 AWS、Azure 和 Google Cloud。

云服务包括计算（EC2、VM）、存储（S3、Blob Storage）、数据库（RDS、Cosmos DB）等。掌握云服务的基础有助于在生产环境中部署应用。

[访问 AWS 文档](https://aws.amazon.com/documentation/) 了解更多。欲了解更多关于云服务的内容，请自行探索。

### Checklist

下面给出一个云服务基础掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道云服务的概念，并能解释 IaaS、PaaS 和 SaaS。
- [ ] 我注册了一个云账户，并能创建虚拟机。
- [ ] 我知道如何使用云存储上传和下载文件。

**基础级：**

- [ ] 我能配置负载均衡器和自动扩展。
- [ ] 我了解云数据库的基本使用。
- [ ] 我知道如何监控云资源的使用和成本。

**进阶级：**

- [ ] 我能设计多区域部署以提高可用性。
- [ ] 我了解无服务器计算（如 Lambda、Functions）。
- [ ] 我知道如何使用 IaC（Infrastructure as Code）工具如 Terraform。

## 备份与恢复

备份和恢复策略是运维中至关重要的一环，用于保护数据免受意外删除、硬件故障、安全事件等威胁。一个好的备份策略应该包括自动化备份、异地存储、定期测试恢复流程等。

常见的备份方案包括数据库备份（mysqldump、pg_dump）、文件系统备份（rsync、tar）、快照备份（云服务商提供）等。还需要考虑备份的频率、保留策略和恢复时间目标（RTO）。

### Checklist

下面给出一个备份与恢复掌握情况的 Checklist，供大家参考：

**新手级：**

- [ ] 我知道为什么备份重要，并了解 3-2-1 备份规则。
- [ ] 我能手动创建数据库或文件系统的备份。
- [ ] 我知道如何从备份中恢复数据。

**基础级：**

- [ ] 我能设置定时自动备份（使用 cron 或 systemd timers）。
- [ ] 我了解完整备份、增量备份和差异备份的区别。
- [ ] 我能将备份存储到远程位置（如云存储、另一台服务器）。

**进阶级：**

- [ ] 我能在 CI/CD 流水线中集成自动化备份。
- [ ] 我了解备份加密和压缩的最佳实践。
- [ ] 我能设计和实施灾难恢复计划（DRP）。
- [ ] 我定期测试备份恢复流程以确保其有效性。


> 本篇文档由 [Fridemn](https://github.com/Fridemn) 编写。
> 封面图片来自 [Kevin](https://kevin56348.github.io/blog/)
> (●'◡'●)