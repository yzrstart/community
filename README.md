<p align="center">
    <img width="150" src="./src/assets/imgs/nice-fish.png">
</p>

<h1 align="center">NiceFish</h1>

<div align="left">
NiceFish（美人鱼） 是一个系列项目，目标是示范前后端分离的开发模式，前端浏览器、移动端、Electron 环境中的各种开发模式，后端有两个版本：SpringBoot 版本和 SpringCloud 版本。
</div>

## 用法

打开终端，依次执行以下命令：

    git clone https://gitee.com/mumu-osc/NiceFish.git
    cd NiceFish
    npm i -g cnpm --registry=https://registry.npm.taobao.org
    cnpm i -g @angular/cli
    cnpm i
    ng serve

打开浏览器，访问http://localhost:4200/

* 各种你懂的原因，中文开发者强烈建议使用 cnpm （淘宝发布的一款npm包装器，方便中文开发者避免一些神秘的问题）
* 如果你想让加载的包更小，请使用参数构建：ng serve --prod
* 构建最终结果：ng build --prod
* 如果之前装过@angular/cli 需要先卸载：npm uninstall -g @angular/cli
* 如果之前装过老版本的 angular-cli 需要先卸载：npm uninstall -g angular-cli
* 如果你之前已经尝试用npm install安装过 node 模块，请把 NiceFish 根目录下的 node_moduels 目录删掉重新 cnpm install
* 命令行删除 node_modules 速度更快，Windows 平台使用： rmdir /s/q node_modules ，*nix平台使用：sudo rm -rf node_modules
* 如果你需要把项目发布到其它类型的 Server 上，例如 Tomcat，需要对 Server 进行一些简单的配置才能支持 HTML5 下的 PushState 路由模式，请从以下链接里面查找对应的配置方式：https://github.com/angular-ui/ui-router/wiki/Frequently-Asked-Questions ，在
How to: Configure your server to work with html5Mode 这个小节里面把常见的 WEB 容器的配置方式都列举出来了，包括：IIS、Apache、nginx、NodeJS、Tomcat 全部都有，你过去抄过来就行。

## 在线演示

- NiceFish 在阿里云上的演示地址: http://47.104.13.149:4200
- NiceFish-React 在gitee上的演示地址：https://mumu-osc.gitee.io/nicefish-react
- OpenWMS 在阿里云上的演示地址：http://47.104.80.251:4200
- OpenWMS 在gitee上的演示地址：https://mumu-osc.gitee.io/openwms-frontend
- NiceFish-ionic：https://damoqiongqiu.github.io/NiceFish-ionic/

## 主要模块选型

- Angular 7.x
- PrimeNG 7.x
- Bootstrap 3.3.7
- Echarts 3.4.0
- ckeditor5-angular

## 界面截图

<img src="./src/assets/imgs/1.png">

<img src="./src/assets/imgs/2.png">

<img src="./src/assets/imgs/3.png">

<img src="./src/assets/imgs/4.png">

## 打包分析

以下是用 webpack-bundle-analyzer 分析打包之后的模块构成：

<img src="./src/assets/imgs/bundle-report.png">

看起来CKEditor和ECharts占了很大的体积，需要做一下异步加载。

webpack-bundle-analyzer 使用方法：

- cnpm i webpack-bundle-analyzer --save-dev
- package.json 的 scripts 配置里面加一行 "bundle-report": "webpack-bundle-analyzer dist/stats.json"
- ng build --prod --stats-json 编译（--stats-json 选项会生成一份stats.json配置文件）
- 执行 npm run bundle-report 查看打包过程

## 学习资源

- 历次演讲中的所有 PPT 已经本项目对应的资料都在这里，您可以随意使用，https://gitee.com/mumu-osc/NiceFish/attach_files 。
- Angular开发者论坛在这里：http://www.ngfans.net/ 。

这是2018年录制的付费视频教程，现在已经过去了快2年，我把它公开出来，免费播放。虽然版本号不是最新的，但是核心的思路和用法基本相同，希望能帮助到有需要的人。

- bilibili 地址：https://www.bilibili.com/video/av87528565
- 油管地址：https://www.youtube.com/watch?v=sIa_KF0cUnE&list=PLbhC27Bf6WlmpDh_66g7Fpn8uCYG7jUn8

## 开源许可证

MIT