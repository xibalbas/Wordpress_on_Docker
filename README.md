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


Finally :) See http://127.0.0.1
#### * Note :

Remember that port 80 must be Free . if you have installed Apache , ngninx , or , httpd 
you must stop these service
