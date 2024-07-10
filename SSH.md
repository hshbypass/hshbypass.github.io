# SSH相关

## authorized_keys

* ed25519

```text
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHgkismKhj76ACVSxr8JQLj8gWSd1HSzXg3ba/p8AsLm
```

记在这里不知道有没有风险:)

## 遇到不支持的情况

```shell
vim ~/.ssh/config
```

Windows下也在一样的地方

```text
Host you_host_name
  KexAlgorithms +diffie-hellman-group1-sha1
  Ciphers +aes256-cbc
```

把不支持的加上再重连就支持了
