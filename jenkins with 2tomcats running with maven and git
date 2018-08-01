#!/bin/bash
cd /tmp/
yum install wget unzip -y
wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm
rpm -ivh jdk-8u131-linux-x64.rpm
wget http://www-eu.apache.org/dist/tomcat/tomcat-8/v8.5.32/bin/apache-tomcat-8.5.32-windows-x64.zip
unzip apache-tomcat-8.5.32-windows-x64.zip
mv apache-tomcat-8.5.32 /opt/tomcat
chmod -R 755 /opt/tomcat/
rm -rf /opt/tomcat/webapps/*
/opt/tomcat/bin/startup.sh
ps -ef | grep tomcat
wget https://updates.jenkins-ci.org/download/war/2.133/jenkins.war
cp jenkins.war /opt/tomcat/webapps/
cd /opt/
cp -r tomcat/ tomcat1 
rm -rf /opt/tomcat1/webapps/*
sed -i 's/8005/8105/g' /opt/tomcat1/conf/server.xml
sed -i 's/8080/8180/g' /opt/tomcat1/conf/server.xml
sed -i 's/8009/8109/g' /opt/tomcat1/conf/server.xml
sed -i 's/8443/8543/g' /opt/tomcat1/conf/server.xml
/opt/tomcat1/bin/startup.sh
ps -ef | grep tomcat
wget http://www-us.apache.org/dist/maven/maven-3/3.5.4/binaries/apache-maven-3.5.4-bin.zip
unzip apache-maven-3.5.4-bin.zip
mv apache-maven-3.5.4 maven
yum install git -y
