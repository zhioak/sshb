# SSH Bastionhost 

连接[奇安信网神运维审计系统](https://www.qianxin.com/product/detail/pid/385)堡垒机，自动完成：

- 2FA两步验证（需要配合`sshenc`）
- 跳转到指定资源
- 执行命令

## ⚙️ Usage

拉取Git仓库到本地

```bash
git clone git@github.com:zhiozhou/sshb.git
```

将命令添加到本地

```bash
sudo cp ~/.ssh/sshb* /usr/local/bin/ 
```

连接堡垒机资源

```bash
sshb -h 127.0.0.1 -r 测试1 -k '~/.totp/bastionhost.key' -c pwd
```

