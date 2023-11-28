# git操作指南

## git 下载安装

下载安装git版本后，使用指令指定用户名和用户邮箱

```shell
git config --global user.name "york"
git config --global user.email "649310717@qq.com"
```

查看全局用户配置

```shell
git config --global user.name
git config --global user.email
```

## ssh密钥对

打开git bash或者cmd，使用以下命令生成ssh密钥对

```shell
ssh-keygen -t rsa -b 4096 -C "649310717@qq.com"
-t rsa 指定要生成 RSA 密钥对。
-b 4096 指定密钥的比特长度（可以根据需要调整）。
-C "your_email@example.com" 可以用您的电子邮件地址替换，这将是用于标识密钥的注释。
```

密钥对生成后会放在.ssh文件夹内，其中系统将为您创建两个文件：`id_rsa`（私钥）和 `id_rsa.pub`（公钥）。私钥是保密的，不应与他人分享，而公钥将用于将您的身份传送给远程 Git 存储库。



## git 命令

```shell
git add .
git commit -m ' '
git push origin master
git pull
git reset --soft
git remote -v         # 查看远程的仓库
git branch            # 列出本地分支
git log 
git status
git checkout [branch_name]
git reset --hard      # 重置工作区到指定提交

//如果工程中包含了不需要进行跟踪的文件类型，可以将文件添加打gitignore中，使用以下命令操作，取消对已经跟随的命令进行调整
git rm --cached -r .
git add .
git commit -m "Remove ignored files from tracking"
```



## sourcetree 可视化git版本管理工具

sourcetree是一款可视化的git版本管理工具，可以与git配合使用，操作更加方便的可视化，如下配置好ssh密钥即可，仓库提交均可视化。

