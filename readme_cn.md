# docker-demo

这个项目是通过一个简单的 python 程序介绍 Dockerfile 和 docker-compose 的使用。

该 Python 程序基于 flask 和 redis 实现了一个 Web 服务。

### 使用说明

#### 环境准备

- 确保 Docker 已安装。[官方安装文档](https://docs.docker.com/engine/install/)
- 确保 Docker Compose 已安装。[官方安装文档](https://docs.docker.com/compose/install/)

检查安装状态

```
docker-compose --version
```

#### 操作步骤

将本项目下载到本地，在项目目录中使用 Compose 命令构建和运行应用。下述命令成功执行完毕后，将完成 docker 镜像构建，启动容器。

```
docker-compose up -d
```

检查容器启动状态
```
docker ps
```

### 常见问题

1. 构建过程遇到报错：network error (check Internet connection and firewall)

这可能是本地代理导致的，可以在项目目录中采用以下命令完成镜像构建。

```
docker build . --network=host
```