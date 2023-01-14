---
title: "Hugo建站（一）"
date: 2023-01-15T00:33:08+08:00
draft: true
---

#### 相关网站

```text
下载: https://github.com/gohugoio/hugo/releases

中文网：https://www.gohugo.org/
中文文档： https://www.gohugo.org/doc/overview/introduction/
官网: https://gohugo.io/


```



#### 安装扩展版本(extended)

- 背景

    有些主题需要扩展版本，否则编译时会报错

```Go
Error: Error building site: TOCSS: failed to transform "scss/style.scss" (text/x-scss): this feature is not available in your current Hugo version

```

    



- 步驟
    1. 下载安装 [7-zip](https://www.7-zip.org/)
    2. 下载[Mingw-w64](https://github.com/niXman/mingw-builds-binaries/releases/latest)。下载名字包含“posix-seh”

        ![](https://secure2.wostatic.cn/static/9SxULqoPkbFtWRrxkM8cXc/image.png?auth_key=1673710963-qXTLULXph3CjSsMSuCefS1-0-1df6e235e2682005be7d63cf0639dd66)

        
    3. 环境变量path添加 mingw64\bin 目录
    4. cmd打开 ，输入gcc —version

        ![](https://secure2.wostatic.cn/static/mxpgrpkubm1yPR4otvXsvi/image.png?auth_key=1673711071-rDCkj784wTdePShyjfHtzh-0-a9967e2717c2f914ff10cce85c593263)

        

    

    1. 安装扩展版本

```Go
go install -tags extended github.com/gohugoio/hugo@latest
hugo version
```

        ![](https://secure2.wostatic.cn/static/9GctmRGSNhS8Kxo2Rwpa4m/image.png?auth_key=1673711240-xvqRsbiDKJBUsob2Au8GNg-0-662b1d03132dd4c6acf84f1ad66390b2)

        

    



#### 常用命令



```text
hugo new site project_dir #在project_dir下新建hugo项目

hugo new about.md #会在项目content目录下新建about.md


- 主题(https://themes.gohugo.io/)
  
  - 选择喜欢的主题
  - cd 项目/themes  git clone xxxx.git
  

- 启动项目
hugo server --theme=主题名  

--baseUrl="http://192.168.56.102/"  # 资源文件访问ip 默认localhost
--bind=0.0.0.0  #默认 127.0.0.1 服务器绑定的入口 
--port=1313  #项目绑定端口 默认1313
hugo --config xxx.yaml  #绑定配置文件  多文件例子: a.toml,b.toml,c.toml



直接运行hugo 会在pubilc 生成静态文本



```





#### 一些主题



```text
https://themes.gohugo.io/themes/hugo-theme-stack/
https://github.com/spf13/hyde
https://themes.gohugo.io/themes/hugo-tranquilpeak-theme/
https://themes.gohugo.io/themes/blackburn/
https://themes.gohugo.io/themes/hugo-theme-stack/

```



#### 使用[stack 主题](https://stack.jimmycai.com/)







#### 自动同步

```text
https://sqh.me/tech/host-hugo-blog-using-caddy/
https://blog.wangjunfeng.com/post/caddy-hugo/

```

