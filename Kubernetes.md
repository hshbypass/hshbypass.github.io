# Kubernetes

## 检查环境

```bash
kubectl version
```

```bash
kubectl cluster-info
```

```bash
kubectl get nodes
```

```bash
kubectl get ingress
```

```bash
kubectl get secrets
```

* 获取Cluster CA证书

```bash
kubectl get secret $(kubectl get secrets | grep default-token | awk '{print $1}') -o jsonpath="{['data']['ca\.crt']}" | base64 --decode
```

* 获取管理用户token

```bash
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin | awk '{print $1}')
```


## 增加节点

```bash
kubeadm token create --print-join-command
```

```bash
curl -fsSL https://get.docker.com -o install-docker.sh
sudo sh install-docker.sh --mirror Aliyun
```

* on CentOS

```bash
yum install -y socat conntrack-tools
```

## 常用操作

### 更新ingress SSL证书

```bash
kubectl get secrets
unzip new_ssl_apache.zip
kubectl get secrets ssl_item -o yaml > 1.yaml
kubectl delete secrets ssl_item
kubectl get secrets
kubectl create secret tls ssl_item --key ssl_item.key --cert ssl_item_chain.crt --cert ssl_item_public.crt
```
