# Máster en Ciencia de Datos e Ingeniería de Computadores. Prácticas de BigData y Cloud Computing. Curso 2017-2018. 

![Header](https://sites.google.com/site/manuparra/home/headerdicits.png)

Manuel J. Parra Royón (manuelparra@decsai.ugr.es) &  José. M. Benítez Sánchez (j.m.benitez@decsai.ugr.es)

[UGR](http://www.ugr.es) | [DICITS](http://dicits.ugr.es) | [SCI2S](http://sci2s.ugr.es) | [DECSAI](http://decsai.ugr.es)


# Exercise with Docker


## Create LDAP client application in PHP

Go to ``betatun.ugr.es``.

Create in your home folder a folder i.e. ```web```:

```mkdir web```

Create a new container:

```docker run -p 15XXX:80 -v /home/CD_XXXXXX/web/:/var/www/html/ --name <your_container_name> -d vaniltonpinheiro/apache-php-ldap```

In this case, we use ``--privileged`` due to SELinux policies on ``betatun.ugr.es``

Go to and check if container is working:

```https://betatun.ugr.es:14XXX/```

Go to the created folder:

```cd /home/CD_XXXXXX/web/```

And create a new file ``index.html`` inside this folder (use a Text Editor like: *vim,vi,pico,...*):

```
vi index.html
```

Write the next:

1. Press key ``i``
2. Paste the next text or write new text:
```
<H1>This is the container service of ManuParra</H1>
```

3. Save the text file, press key ``ESC`` and then write ``:wq`` and press key ``Intro``.



And open your browser with the next URL:

```http://betatun:15XXX/```

*Remember: use your Port Assignment  ``cat puertosdocker.txt``*

You will see the text created from the webserver on the container.
