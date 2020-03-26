# Ansible

##  官网

https://www.ansible.com/resources/get-started    





#####  Reference:

######  ansible起步指南   
https://yq.aliyun.com/articles/86760?t=t1   





#  基础使用

##  安装

```
yum -y install  ansible
```



## 配置

###  配置免密登录

```
ssh-keygen -t rsa
```

```
ssh-copy-id -i ~/.ssh/id_rsa.pub root@1.2.3.4
```



###  配置hosts文件

```
vim /etc/ansible/hosts

```


####  hosts文件验证
```
ansible-inventory --list -y

```




##  测试

```
 ansible all -m ping

```

##  基础命令

```
各台机器执行 echo hello  ansible 命令
ansible all -m shell -a '/bin/echo hello ansible'

```



# Playbook

```
ansible-playbook     hello-world.yml

```




#  实例

##  ansible安装docker

```
 ansible all -m shell -a 'wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo'
```



