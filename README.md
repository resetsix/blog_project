### 拉取项目

```bash
$ git clone https://gitee.com/resetsix_admin/blog
```

### 安装依赖

```bash
$ npm i -g yarn
$ cd blog
$ yarn
```

### 启动项目

```bash
$ yarn clean && yarn build && yarn server
```

或者

```bash
$ hexo clean && hexo g && hexo s
```

### 部署到 github page

执行

```bash
$ yarn add hexo-deployer-git
```

修改\_config.yml 配置文件，在文件最底部添加如下配置：（要求：用户名和仓库名保持一致）

```yaml
deploy:
  type: git
  # repo: https://github.com/用户名/仓库名.github.io.git
  repo: git@github.com:resetsix/resetsix.github.io.git
  branch: master
```

最后执行

```bash
hexo g -d
```

执行代码 github 会自动编译代码，执行之后稍等片刻，即能访问地址 https://Github 用户名.github.io/
完结。
