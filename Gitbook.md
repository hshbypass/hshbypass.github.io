# Gitbook

碎碎念：
把markdown文件转换为网页，挺好玩的

```bash
npm install -g gitbook-cli
gitbook init
```

Node.js太烦人了，各种问题

## Windows系统下使用

* 遇到问题，未搞定

## Linux系统下使用

* 遇到问题，未搞定

## Docker环境下使用

### 准备环境

* Gitbook

```bash
docker run -d --name gitbook -v /home/admin/github/gitbook:/srv/gitbook -v /home/admin/github/html:/srv/html fellah/gitbook
```

* Nginx

```bash
docker run --name nginx-gitbook -v /home/admin/github/html:/usr/share/nginx/html -d -p 80:80 nginx
```

### 使用

```bash
docker exec -it gitbook /bin/bash

gitbook build . /srv/html/
```

![gitbook_build](https://hshbypass.github.io/picx-images-hosting/pics/gitbook_build.4jnzedsai8.jpg)

Nginx运行状态下直接刷新网页即可
