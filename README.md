# ios
电脑上调试ios手机

1.下载iTunes
https://www.apple.com/itunes/
点击下载64位的即可

2.安装ios_webkit_debug_proxy
安装scoop（一个安装工具），在powershell应用中运行如下命令
   set-executionpolicy unrestricted -s cu            //修改执行策略，选择是
   iex (new-object net.webclient).downloadstring('https://get.scoop.sh')         //安装scoop
 安装ios_webkit_debug_proxy，在powershell应用中运行如下命令
    scoop bucket add extras
    scoop install ios-webkit-debug-proxy

3.使用npm下载最新版本的调试器
（需要node.js环境）
npm install remotedebug-ios-webkit-adapter -g

4.打开iOS设备的
设置—>Safari浏览器—>高级—>将网页检查器打开

5.用任意一种的命令行工具运行适配器（插件）
比如：CMD、PowerShell
remotedebug_ios_webkit_adapter --port=9000

6.你可以通过利用Chrome浏览器调试工具，让你的iOS页面目标显示在Chrome的chrome://inspect/#devices页面中，需要添加运行适配器的计算机的IP，如localhost:9000。

7.点击inspect就可以轻松调试设备了~
