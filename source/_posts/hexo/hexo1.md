---
title: Hexo使用
categories: 
 - Hexo
tags:
 - Hexo
data: 2022-03-21 11:01:00
index_img: https://instrument-file.oss-cn-beijing.aliyuncs.com/img/logo.png?x-oss-process=image/resize,m_pad,w_268,h_160/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_south,x_10,y_10
---
### 什么是 Hexo

> Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

### 安装(windows环境)

> Hexo 安装版本相关信息
    hexo: 5.4.1
    hexo-cli: 4.3.0
    os: win32 10.0.22000
    node: 16.14.0
    v8: 9.4.146.24-node.20
    uv: 1.43.0
    zlib: 1.2.11
    brotli: 1.0.9
    ares: 1.18.1
    modules: 93
    nghttp2: 1.45.1
    napi: 8
    llhttp: 6.0.4
    openssl: 1.1.1m+quic
    cldr: 40.0
    icu: 70.1
    tz: 2021a3
    unicode: 14.0
    ngtcp2: 0.1.0-DEV
    nghttp3: 0.1.0-DEV

#### 1.安装Node.js

- [Node.js中文网](http://nodejs.cn/)
- [Node.js官网](https://nodejs.org/zh-cn/)

#### 2.安装Git

- [Git官网](https://git-scm.com/)

#### 3.安装Hexo

1. 所有必备的应用程序安装完成后，即可使用 npm 安装 Hexo。

    ```bash
    npm install -g hexo-cli
    ```

2. 进阶安装和使用,对于熟悉 npm 的进阶用户，可以仅局部安装 hexo 包。

    ```bash
    npm install hexo
    ```

    {% gi total n1-n2-... %}
    ![进行中图示](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321143138.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

    ![成功后图示](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321143158.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)
    {% endgi %}

3. 安装以后，可以使用以下两种方式执行 Hexo：
    1. `npx hexo <command>`

        ```bash
        Usage: hexo <command>

        Commands:

        help     在一个命令上获得帮助。
        init     创建一个新的Hexo文件夹。
        version  显示版本信息。
        
        Global Options:

        --config  指定配置文件，而不是使用 _config.yml
        --cwd     指定CWD
        --debug   在终端显示所有粗略的信息
        --draft   显示帖子草稿
        --safe    禁用所有插件和脚本
        --silent  隐藏控制台中的输出
        如需更多帮助，你可以使用 "hexo help [command]"获得详细信息
        或者你可以查看文档：http://hexo.io/docs/
        ```

    2. 将 Hexo 所在的目录下的 node_modules 添加到环境变量之中即可直接使用 `hexo <command>`：

        ``` bash
        echo 'PATH="$PATH:./node_modules/.bin"' >> ~/.profile
        ```

    3. 注意事项
        > Node.js 版本限制
        我们强烈建议永远安装最新版本的 Hexo，以及 推荐的 [Node.js](https://hexo.io/zh-cn/docs/#%E5%AE%89%E8%A3%85%E5%89%8D%E6%8F%90) 版本。

        ![图示](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321144759.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

### 建站

#### 1. `hexo init <folder>`

```bash
# 因为没有把Hexo目录下的node_modules添加到环境变量所以需要npx
npx hexo init hexo
# 成功后
INFO  Cloning hexo-starter https://github.com/hexojs/hexo-starter.git
INFO  Install dependencies
INFO  Start blogging with Hexo!
```

![图示1](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321145259.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

##### 2. 成功以后通过命令行进入对应文件夹 `cd <folder>`

![文件夹内图示](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321145709.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

#### 3. 通过命令行执行 `npm install`

#### 4. 配置 `_config.yml` 依据[官方中文文档配置](https://hexo.io/zh-cn/docs/

#### configuration)

#### 5. 运行hexo

- 可以通过[vscode](https://code.visualstudio.com/)打开根目录,执行npm脚本`server hexo server`

    > **注**:可能需要安装插件 [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script); [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)

- 或者通过命令运行hexo

    ```bash
    PS E:\test\hexo> npx hexo server
    INFO  Validating config
    INFO  Start processing
    INFO  Hexo is running at http://localhost:4000/ . Press Ctrl+C to stop.
    ```

    通过访问[http://localhost:4000/](http://localhost:4000/)在浏览器中查看

    ![hexo默认主题展示](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321151723.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

#### 6. 指令

```bash
# 生成静态文件。
hexo generate 
# 清除缓存文件 db.json 和已生成的静态文件 public。
hexo clean
# 部署网站。
hexo deploy
# 启动服务器。默认情况下，访问网址为： http://localhost:4000/。
hexo server
```

更多指令详细信息可以访问官网[指令](https://hexo.io/zh-cn/docs/commands)

### 来源

[Hexo中文官网](https://hexo.io/zh-cn/)
