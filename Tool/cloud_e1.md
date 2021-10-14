# 云计算实验

## 主机配置

贵阳 1 1区 139.9.251.249

Tomcat 

下载  jdk包和tomcat包

在/usr/local解压 [jdk-8u301-linux-x64.tar.gz](jdk-8u301-linux-x64.tar.gz)  [apache-tomcat-8.5.71.tar.gz](apache-tomcat-8.5.71.tar.gz) 

```shell
tar -xvf jdk-8u301-linux-x64.tar.gz

tar -xvf apache-tomcat-8.5.71.tar.gz

vi /etc/profile
添加
export JAVA_HOME=/usr/local/jdk1.8.0_301  
export JRE_HOME=${JAVA_HOME}/jre  
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib  
export PATH=${JAVA_HOME}/bin:$PATH

source /etc/profile

cd /usr/local/tomcat/bin

vi setclasspath.sh
添加
export JAVA_HOME=/usr/local/jdk1.8.0_301  
export JRE_HOME=${JAVA_HOME}/jre

把tomcatxxxx文件夹名字改为tomcat
cd /usr/local/tomcat/bin
./startup.sh

查看 服务器ip：8080（前提是安全组里8080端口打开）
添加规则 8080即可
cd /usr/local/tomcat/webapps/ROOT

vi index.html 
编写即可

重启实例
cd /usr/local/tomcat/bin
./startup.sh
查看 服务器ip：8080（前提是安全组里8080端口打开）
```



关于对象存储

[新建文件夹_对象存储服务 OBS_控制台指南_管理对象_华为云 (huaweicloud.com)](https://support.huaweicloud.com/usermanual-obs/obs_03_0316.html)

注意设置公共访问权限

A 贵阳一 1区

B 贵阳一 4区

C 乌兰察布 1区





