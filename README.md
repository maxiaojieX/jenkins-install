
# Jenkins Install

<hr>

一、安装教程地址推荐
1、CentOS
https://linuxize.com/post/how-to-install-jenkins-on-centos-7/

2、Ubuntu
https://linuxize.com/post/how-to-install-jenkins-on-ubuntu-18-04/


二、启动
java -jar jenkins.war --ajp13Port=-1 --httpPort=8083

三、安装插件
1）	Subversion Plug-in
拉取SVN代码
2）Publish Over SSH
传文件到指定服务器
3）SSH Agent
SSH秘钥代理
4）build-name-setter
设置构建名称

四、全局配置
1、配置JDK路径、maven_home
2、配置SSH密钥连接及服务器

五、问题记录
1、jenkins执行完构建命令会杀死当前构建进程以及其衍生进程，所以启动jar完成时会被jenkins杀死。解决办法：在exe shell command头部加上BUILD_ID=DONTKILLME
2、执行linux 自定义shell时找不到shell中定义的自定义命令，例如在linux上自定义命令，命令"abc" > cd /abc,jenkins报abc命令找不到。解决办法：在自定义shell头部使用#!/bin/bash -iel注解

