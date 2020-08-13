# AWS EC2 Ubuntu Server

## Ubuntu에 파일 옮기기 scp
1. ssh connect
    + ssh -i "pem_file_route" ubuntu@ec2_instance_IP
2. send_target_file
   + upload 할 file 경로로 이동
   + scp -i "pem_file_route" target_file_name ubuntu@ec2_instance_IP:~[route]

## Ubuntu_update
1. update
    + sudo apt-get update
2. upgrage
    + sudo apt-get upgrade

## Ubuntu_unzip
1. install unzip
    + sudo apt-get install unzip
2. use unzip
    + unzip [target_zipFile].zip

## install_ORACLE
1. sudo apt-get install alien libaio1 unixodbc