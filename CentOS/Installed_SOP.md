# Initial

## SSH

```bash
mkdir ~/.ssh
touch ~/.ssh/authorized_keys
echo "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHgkismKhj76ACVSxr8JQLj8gWSd1HSzXg3ba/p8AsLm" | tee -a ~/.ssh/authorized_keys

sed -i 's/#baseurl\=/baseurl\=/g' /etc/yum.repos.d/CentOS-Base.repo
sed -i 's/mirror.centos.org/mirrors.aliyun.com/g' /etc/yum.repos.d/CentOS-Base.repo
sed -i 's/mirrorlist\=/#mirrorlist\=/g' /etc/yum.repos.d/CentOS-Base.repo

sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/sysconfig/selinux

systemctl stop firewalld && systemctl disable firewalld

yum check-update
yum update -y
yum install -y open-vm-tools vim sysstat

```
