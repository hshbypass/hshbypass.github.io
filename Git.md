# Git

## Git基本使用

```bash
git config --global user.name you_user_name
git config --global user.email you_user_name@you_mail.domain
```

* 建好自己的仓库

* 本地init

```bash
cd you_dir
git init
```

* 关联远端仓库

```bash
git remote add origin https://github.com/you_user_name/you_repo.git
```

* 暂存本地文件到缓冲区

```bash
git add .
```

* 填写描述

```bash
git commit -m "Initial"
```

* 推送

```bash
git push -u origin --all
```
