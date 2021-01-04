# build my blog on github pages



## 1 在网页创建github账户

此处略



## 2 在电脑安装、配置git

### 2.1 安装git

1. 下载git 64bit版本，并 安装

2. 开始菜单 > Git > Git Bash，打开

3. 键入命令，查看git版本号。

```
git --version
```

### 2.2 配置密钥

为什么要使用密钥，及如何配置密钥查看这里：

GIT为什么要配置公钥和私钥-简书

### 2.3 设置用户名和邮箱

如何设置请查看"github git cheat sheet"中的CONFIGURE TOOLING。前两条必须：

```
$ git config --global user.name "[name]"
$ git config --global user.email "[email address]"
```

至此，git部分设置完毕。



## 3 创建github pages

如何创建及如何测试查看这里：[Github Pages](https://pages.github.com/)。



## 4 使用Hexo

参考[hexo官方网站](https://hexo.io/)，具体如下：

### 4.1 安装Hexo

```
$ npm install hexo-cli -g
```

### 4.2 创建hexo文件夹

```
$ mkdir ~/hexo`
`$ cd ~/hexo
```

### 4.3 初始化hexo 网站，即创建全新的hexo站点文件。

查看官方文档：[setup](https://hexo.io/docs/setup)

### 4.4 设置hexo配置文件`_config.yml`，使hexo与git连接。

查看官方文档：[configuration](https://hexo.io/docs/configuration)

### 4.5 安装部署插件。

```
$ npm install hexo-deployer-git --save
```



## 5 常见操作

### 5.1 创建新的博文

1. 进入hexo创建的站点文件夹，比如：`~/hexo/<folder>`

2. 删除hexo的缓存文件：`$ hexo clean`

3. 创建新的post：`$ hexo new "我的第一个博文"`

4. 修改博文：`cd source/_posts/`，`notepad '我的第一个博文'`并保存。

5. 生成静态文件：`hexo generate`

6. 部署到github pages：`hexo deploy`

7. 完成。

### 5.2 预览博文

```
$ hexo server
```

创建本地服务器，在浏览器输入

```
http://localhost:4000
```

进行预览。

### 5.3 需要备份保存的文件：

- 密钥：`~/.ssh`
- hexo配置文件：`~/hexo/<folder>/_config.yml`
- 全站保存：`~/hexo/*`