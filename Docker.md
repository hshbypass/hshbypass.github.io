---
description: Docker安装及初步配置
---

# Docker

## Docker

### Docker安装

* 安装代码所在网址[https://get.docker.com/](https://get.docker.com/)
* 安装过程

```bash
curl -fsSL https://get.docker.com -o install-docker.sh
cat install-docker.sh
sudo sh install-docker.sh --mirror AzureChinaCloud
```

* 将当前用户加入docker组

```bash
sudo vim /etc/group
```

* 注销后重新登陆
* 验证Docker安装

```bash
docker run hello-world
```

如果代码正常运行，则示例如下：

![docker_hello_world](https://hshbypass.github.io/picx-images-hosting/pics/docker_hello_world.8z6ejjna29.jpg)

### 异常处理

如果docker pull一直搞不回来，有几个方案

1. 切换为国内源
2. (如果没有国内源)搞个免墙服务器pull完打标签再push到国内可以访问的registry里
2. 搞资源搭一个registry的proxy

#### 切换为国内源

以后再补

#### pull&tag&push

以下为示例，用的阿里云的Registry，有自己的也可以用自己的

* OK的服务器

```bash
docker pull hello-world
docker tag d2c94e258dcb registry.cn-beijing.aliyuncs.com/you_user_name/hello-world:latest
docker push registry.cn-beijing.aliyuncs.com/you_user_name/hello-world:latest
```

别忘了登录registry

```bash
docker login --username=you_user_name registry.cn-beijing.aliyuncs.com
```

* 直接连不上的服务器

```bash
docker pull registry.cn-beijing.aliyuncs.com/you_user_name/hello-world:latest
```

#### 搞资源搭Registry的Proxy

以后再补

