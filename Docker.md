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
