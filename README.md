# github的简单操作
1.首先注册一个自己的github账号，并配置ssh key，Mac机的配置地址如下

(https://jingyan.baidu.com/article/6c67b1d6b19e892786bb1e49.html)；

2.关于ssh服务的启动(以后提交代码的时候不用总输入账号密码啥的)：
mac本身安装了ssh服务，默认情况下不会开机自启:
```javascript
// 1、启动sshd服务：
$ sudo launchctl load -w /System/Library/LaunchDaemons/ssh.plist
//2、停止sshd服务：
$ sudo launchctl unload -w /System/Library/LaunchDaemons/ssh.plist
//3、查看是否启动：
$ sudo launchctl list | grep ssh
//如果看到下面的输出表示成功启动了：
- 0  com.openssh.sshd
```
3.一些简单的操作：
```javascript
cd //至文件夹中之后
echo "# example1" >> README.md      //--创建一个README.md 的文件

ls    //--显示当前目录的内容

git init    //-- 本地初始化这个仓库，让远程知道你这是git仓库。

git add .  //--添加所有改动的东西

git commit -m "first commit 第一次提交代码"    //-- 提交代码

git remote add origin https://github.com/Tokenfire/example1.git     --关联远程仓库，
将本地的仓库和github的远程仓库给关联起来了

git push -u origin master    // 将代码push到远程仓库中

```

