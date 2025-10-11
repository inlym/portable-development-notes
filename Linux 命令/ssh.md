# ssh 系列命令

## 命令集合

| 序号 | 命令        | 用途                     |
| ---- | ----------- | ------------------------ |
| 1    | ssh         | 访问远程主机             |
| 2    | ssh-keygen  | 生成 SSH 密钥            |
| 3    | ssh-copy-id | 将公钥文件复制到远程主机 |
| 4    | scp         | 与远程主机之间复制文件   |

## 命令实例

演示各个命令的常用用法。

### ssh

普通连接

```bash
ssh username@remote_host
```

指定端口

```bash
ssh -p 2211 username@remote_host
```

### ssh-keygen

使用 ed25519 算法生成密钥（并指定注释信息）

```bash
ssh-keygen -t ed25519 -C "message"
```

使用 RSA 算法生成密钥（并指定注释信息）

```bash
ssh-keygen -t rsa -b 4096 -C "message"
```

### ssh-copy-id

普通用法

```bash
ssh-copy-id username@remote_host
```

### scp

从远程主机复制文件到本地目录

```bash
scp username@remote_host:/opt/soft/nginx-0.5.38.tar.gz /opt/soft/
```

上传本地目录到远程机器指定目录

```bash
scp -r /opt/soft/mongodb username@remote_host:/opt/soft/scptest
```
