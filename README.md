# WordPress on Docker

an easy way to rapid start a wordpress project on any VM with Containers

## Getting Started 



#### 1. install Docker And Docker-compose on your system 

* For `Ubunto`
```bash
$ sudo apt install docker.io
$ sudo apt install docker-compose
```
#### 2. Create Volumes And Networks on your System

* Create `volumes`
```bash
$ sudo docker volume create db_data

```
* Create `Networks`
```bash
$ sudo docker network create wpsite
```
* Run `docker-composers`

```bash
$ git clone https://github.com/jupidev-code/Wordpress_on_Docker.git
$ cd Wordpress_on_Docker/ 
$ sudo docker-compose up -d

```

* See Logs 

```bash
# First see Whats the name of wordpress container with this

$ sudo docker ps -a     # it will show all of your container

$ sudo docker logs <container_name>

```
* Solve Upload Limite
```bash
$ docker container exec -it 9ddd9bded663 bash -c "echo 'php_value upload_max_filesize 256M' > '/var/www/html/.htaccess'"
```

http://127.0.0.1  ==> Wordpress 

http://127.0.0.1:8080  ==> phpmyadmin

Finally 
#### * Note :

* Remember that port 80 must be Free . if you have installed Apache , ngninx , or , httpd 
you must stop these service

* you can change your DataBase Password From .yml file
