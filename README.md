# 011springboot+vue教室图书馆预约管理系统
011springboot+vue教室图书馆预约管理系统

## 项目简介：

这是一个前后端分离的教室预约和查看系统项目，能够实现以教室为单位活动的预约和取消，能够以视图形式显示，附带图书馆和公告管理器功能。
主要采用`Vue.js`+`SpringBoot` 技术栈开发

* 使用技术点

* 前端：`Vue`、`ElementUI`、`axios`、`Echart`、`jQurey`
* 后端：`SpringBoot`、`Spring Data + JPA`、`hibernate`、`MySQL`、`Shiro`、`Redis`

源码获取：[ **点此获取** ](http://www.shuyue.fun/index.php?type=productinfo&id=160)

## 使用说明：
1. 在mysql数据库中创建数据库`testmeeting`行项目，将自动注入数据。如需关闭此功能，请将 `application.properties `中的
`spring.datasource.initialization-mode=always` 代码注释。同样，可以通过使用项目`sql`目录下`testmeeting`直接导入数
据库数据结构与内容，可根据需要自行使用。`Redis 端口为 6379（默认端口），密码为空。`

2. 数据库配置在后端项目的 src\main\resources 目录下的application.properties 文件中，mysql 版本为 8.0以上版本 。

3. 在IntelliJ IDEA中运行后端项目，为了保证项目成功运行，可以右键点击 pom.xml 选择 maven -> reimport ，并重启项目。
至此，服务端就启动成功了，同时，运行前端项目，访问 http://localhost:8080 ，即可进入登录页面，默认账号是 admin，密码是 123

4. 项目使用了虹软公司的人脸识别SDK与百度的人体分析SDk：
* 虹软的SDK请自行前往官网获取，获取后建议将SDK导入到``src/main/resources/lib-sdk``目录下,然后在``src/main/java/utils``目录下新建``SdkParameter.java``文件，填入appId和key以及引擎和算法等文件位置。

* 百度人体分析SDk已在``maven``中引用，但是``app_id``等请前往百度云AI开发者平台自行获取，该项目中表示位置为``SdkParameter.java``文件。

* 以上内容不必要，可以删除并注释对应接口与服务即可。
----

## 二次开发请注意：

* 进入前端项目根目录中，在命令行依次输入如下命令：

```text
# 安装依赖
npm install

# 在 localhost:8080 启动项目
npm run dev
```

* 由于在前端项目中已经配置了端口转发，将数据转发到SpringBoot上，因此项目启动之后，在浏览器中输入 `http://localhost:8080`
就可以访问我们的前端项目了，所有的请求通过端口转发将数据传到 SpringBoot 中（注意此时不要关闭 SpringBoot 项目）。

* 最后可以用 IDEA / WebStorm 等工具打开前端项目，继续开发，开发完成后，当项目要上线时，依然进入到 wj-vue 目录，然后执行如下命令：

```text
npm run build
```

* 该命令执行成功之后，前端项目目录下生成一个 `dist` 文件夹，可以将该文件夹中的两个文件` static `和 `index.html`
拷贝到前端项目中 `resources/static/ `目录下，然后直接运行前端项目，访问 `http://localhost:8443` ，
实际上是把前端打包后作为静态文件，但不推荐使用这种方式。

## 运行截图
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/002215_fb458b01_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/002254_6b223951_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/002814_7602a505_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/002827_4dcfd599_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105001_378ebbb3_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105010_3ea1da65_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105022_0844f874_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105030_35701ba8_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105038_3de2bad6_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105045_68c1b9fd_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0319/105054_0634f220_863230.png "屏幕截图.png")
