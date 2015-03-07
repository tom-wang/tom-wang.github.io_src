title: 基于Hexo博客生成系统搭建GitHub Pages博客
tag:
  - 生活
  - 随笔
---
最近在GitHub上搭建了自己的博客，开篇文章就把自己搭建博客的过程分享给大家吧

对于码工来说，GitHub大部分人都用过，[GitHub
Pages](https://pages.github.com/)可能大部分人没有实操过。它是GitHub提供的一个静态文件托管服务，最常见的是将博客托管在它上面，类似以前我们用过的虚拟主机，但是文件管理方式略有不同，传统的虚拟主机是将文件通过FTP方式提交，GitHub Pages将文件管理和GitHub项目融合在一起，向指定的项目里提交文件即达到了管理文件的目的。它仅托管静态页面，所以在写博客时需要我们自己先生成好html文件再发布。

生成静态页面的程序有很多，例如<!--more-->`Jekyll`、`Octopress`、`Hexo`等等，Hexo是NodeJS程序，对于前端码工来说更加亲切一些，因此我的博客采用了Hexo。

整个博客的搭建分为以下步骤：
* 注册GitHub账户，创建项目
* 安装、使用Hexo

## 注册GitHub账户，创建项目

### 注册GitHub账户
这个不用多说，没有账户的OutMan浏览到这里就可以了

### 创建项目
项目的名字必须严格按照规范命名为`username.github.io`（将username换成你的GitHub账户名），这个名字同时也是专属你的子域名（取一个好名字多么重要！），如下
![name-as-username](/images/hello-world/name-as-username.png)

### Hello World
添加一个静态页面，提交之后即可到浏览器输入你的专属域名进行验证

**到这里博客已经搭建成功了，我们还需要使用静态页面生成器来生成页面，突显高逼格。接下来为大家介绍Hexo。**

## 安装、使用[Hexo](https://github.com/hexojs/hexo-cli)

### 安装Hexo
``` bash
$ npm install hexo-cli -g
```

### 初始化项目

``` bash
$ cd your_blog_dir

# 等同于hexo i
$ hexo init
INFO  Copying data to ~/github/test
INFO  You are almost done! Don't forget to run 'npm install' before you start blogging with Hexo!

$ npm install
```

### 新增页面

``` bash
# 等同于hexo n "new post title"
$ hexo new "new post title"
```

### 生成静态文件

``` bash
# 等同于hexo g
$ hexo generate
```

最后，将生成的静态页面提交到GitHub就OK啦

### 配置Hexo

Hexo支持配置插件、主题，配置文件是_config.yml，插件主题也可以有自己的_config.yml。除官方主题外还有第三方开发者开发的主题，大家可以找个逼格高的主题。
