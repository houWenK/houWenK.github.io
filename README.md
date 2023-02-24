# houWenK.github.io

侯文科的个人博客(hexo+github)https://houwenk.github.io/

## 1.准备 ##

下载并安装code,git

## 2.hexo下载

hexo下载：

```
npm install express -g
```

检测是否成功

```
hexo -v
```

## 3.ssh绑定

生成ssh:ssh-keygen -t rsa -C "邮箱地址"

.ssh生成路径：C:\Users\你他娘的用户名\.ssh

测定ssh是否绑定成功：

```
ssh -T git@github.com
```

如果一直出现ssh: connect to host github.com port 22: Connection refused的话具体看这个教程https://www.cnblogs.com/Archer314/p/14641310.html

## 4.初始化hexo

初始化hexo博客

```
hexo init
```

如果报错SyntaxError: Unexpected token ...

建议更新一下node.js版本

静态生成hexo页面

```
hexo s
```

## 5.修改配置文件

配置文件修改(_config.yml)

deploy:

 type: git

 repository:https://github.com/你的名字/仓库的名字.git

 branch: 分支

## 6.发布

安装hexo-deployer-git自动部署发布工具:

```
npm install hexo-deployer-git --save
```

生成静态文件

```
hexo g
```

发送到github

```
hexo d
```

