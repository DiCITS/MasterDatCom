# Máster en Ciencia de Datos e Ingeniería de Computadores. Prácticas de BigData y Cloud Computing. Curso 2017-2018. 

![Header](https://sites.google.com/site/manuparra/home/headerdicits.png)

Manuel J. Parra Royón (manuelparra@decsai.ugr.es) &  José. M. Benítez Sánchez (j.m.benitez@decsai.ugr.es)

[UGR](http://www.ugr.es) | [DICITS](http://dicits.ugr.es) | [SCI2S](http://sci2s.ugr.es) | [DECSAI](http://decsai.ugr.es)


# Exercise with OpenNebula and OpenStack


## Create a RService 

Go to ``docker.ugr.es`` or ``atcstack.ugr.es``.

Create a Virtual Machine with CentOS7 or CentOS6.

Once started the Virtual Machine, use ssh to connect:

```
ssh root@192.168.10.XXX
```

Install the next:

```
yum install epel-release
```

then 

```
yum install R -y
```

Install inside R your favorite packages.


## Create a Web Service 

In one of your VM, install :

A) WebServer:

```
sudo yum install httpd
sudo systemctl start httpd.service
sudo systemctl enable httpd.service
```

B) PHP:

```
sudo yum install php php-mysql
sudo systemctl restart httpd.service
```

Exit of the VM and create another VM (your mate's VM) for MySQL Server (MariaSQL)


## Create a MySQL (DataBase) service

In one of your VM (mate), install :

```
sudo yum install mariadb-server mariadb
sudo systemctl start mariadb
```

Configure MySQL Database Service:

```
sudo mysql_secure_installation
```

Enable Service:

```
sudo systemctl enable mariadb.service
```

## Create full service

Connect WebServer VirtualMachine with MySQL DataBase Service 



