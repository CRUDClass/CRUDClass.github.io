---
title: Hexo主题之Fluid
categories: 
 - [Hexo,Fluid主题]
tags:
 - Hexo
data: 2022-03-21 16:40:00
index_img: https://instrument-file.oss-cn-beijing.aliyuncs.com/img/3419353.png?x-oss-process=image/resize,m_pad,w_268,h_160/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_south,x_10,y_10
---

### Fluid简介

一款 Material Design 风格的 Hexo 博客主题

![https://hexo.fluid-dev.com/](https://instrument-file.oss-cn-beijing.aliyuncs.com/img/20220321172250.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5na2FpdGk,size_20,text_QOmxvOWtkOmFsQ==,color_012EA5,shadow_0,t_100,g_se,x_10,y_10)

### 安装主题(version：1.8.14)

Hexo 5.0.0 版本以上，推荐通过 npm 直接安装，进入博客根目录执行命令：

```bash
npm install --save hexo-theme-fluid
```

然后在博客目录下创建 `_config.fluid.yml`，将主题的 [`_config.yml`](https://github.com/fluid-dev/hexo-theme-fluid/blob/master/_config.yml)内容复制过去。

{% note warning %}
`_config.fluid.yml`和hexo的`_config.yml`同级,可以根据个人需求配置主题相关内容,无法访问可以查看博客**Hexo Fluid主题_config.yml**
{% endnote %}

### 指定主题

如下修改 Hexo 博客目录中的 `_config.yml`：

```yml
theme: fluid  # 指定主题

language: zh-CN  # 指定语言，会影响主题显示的语言，按需修改
```

### 创建「关于页」

首次使用主题的「关于页」需要手动创建：

```yml
hexo new page about
```

创建成功后修改 `/source/about/index.md`，添加 `layout` 属性。

修改后的文件示例如下：

```md
---
title: 标题
layout: about
---

这里写关于页的正文，支持 Markdown, HTML
```

{% note warning %}
`layout: about` 必须存在，并且不能修改成其他值，否则不会显示头像等样式。
{% endnote %}

### 其他

更详细的配置信息等请参考[官方文档](https://hexo.fluid-dev.com/docs/)

### 来源

- [Hexo Fluid GitHub](https://github.com/fluid-dev/hexo-theme-fluid)
- [Hexo Fluid 用户手册](https://hexo.fluid-dev.com/docs/)
- [Fluid's blog](https://hexo.fluid-dev.com/)
