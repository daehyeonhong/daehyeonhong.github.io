# AWS EC2 Ubuntu Server

## install_OpenJDK8

1. version_check_Java
   - java -version
2. install_OpenJDK8
   - sudo apt-get install openjdk-8-jdk
3. 1. version_check_Java
   - java -version
   - javac -version
4. check_path_javac
   - witch javac
5. check_realPath_javac
   - readlink -f javac_path
6. #profile
   - sudo nano /etc/profile
     - export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
     - export PATH=$JAVA_HOME/bin/:$PATH
     - export CLASS_PATH=$JAVA_HOME/lib/:$CLASS_PATH
7. reload_profile
   - source /etc/profile
8. reboot ubuntu
   - reboot now
9. check environment variable
   - echo \$JAVA_HOME

## Ubuntu에 파일 옮기기 scp

1. ssh connect
   - ssh -i "pem_file_path" ubuntu@ec2_instance_IP
2. send_target_file
   - upload 할 file 경로로 이동
   - scp -i "pem_file_path" target_file_name ubuntu@ec2_instance_IP:~[path]

## Ubuntu_update

1. update
   - sudo apt-get update
2. upgrage
   - sudo apt-get upgrade

## Ubuntu_unzip

1. install unzip
   - sudo apt-get install unzip
2. use unzip
   - unzip [target_zipFile].zip

## install_ORACLE

1. sudo apt-get install alien libaio1 unixodbc
2. convert .rpm-->.deb
   - alien --scripts -d oracle\*
3. install_oracle
   - sudo dpkg --install oracle\*.deb
4. setting_oracle_configure
   - /etc/init.d/oracle-xe configure
5. setting_oracle_environment_variable
   - . /u01/app/oracle/product/11.2.0/xe/bin/oracle_env.sh
   - sudo /etc/bash.bashrc
6. connect_oracle
   - sqlpus system

## install_tomcat8

1. sudo apt-get install tomcat8
2. change_server_port
<<<<<<< HEAD
    + sudo vi /var/lib/tomact8/conf/server.xml
    \<Connector port="XXXX"\>

## Oracle_Error
1. Lsnrctl services
=======
   - sudo vi /var/lib/tomact8/conf/server.xml
     \<Connector port="XXXX"\>

## install_MySQL

1. install_MySQL
   - sudo apt-get install
     update mysql.user set plugin='mysql_native_password' where user='root';

update mysql.user set authentication_string=PASSWORD('password') where user='root';
flush privileges;
quit

3. change_bind-address

   - sudo vi /etc/mysql/mysql.conf.d/mysql.cnf

4. setting_default_characterSet
   - MySQL> CREATE DATABASE [DATABASE_NAME] DEFAULT CHARACTER SET UTF8 COLLATE UTF8_GENERAL_CI;

## install_mysql-connector-java.jar

1. install_jstl

   - apt-get install libmysql-java

2. link_tomcat8
   - ln -s /usr/share/java/mysql-connector-java.jar /usr/share/tomcat8/lib/mysql-connector-java.jar
>>>>>>> 69d3a3b34155aa357170741d4742fa767a13c55a
