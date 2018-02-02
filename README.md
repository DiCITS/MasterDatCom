# Máster en Ciencia de Datos e Ingeniería de Computadores. Prácticas de BigData y Cloud Computing. Curso 2017-2018. 

![Header](https://sites.google.com/site/manuparra/home/headerdicits.png)

Manuel J. Parra Royón (manuelparra@decsai.ugr.es) &  José. M. Benítez Sánchez (j.m.benitez@decsai.ugr.es)

[UGR](http://www.ugr.es) | [DICITS](http://dicits.ugr.es) | [SCI2S](http://sci2s.ugr.es) | [DECSAI](http://decsai.ugr.es)


Table of Contents
=================


   * [1. Environment of the practice](#environment-of-the-practice)
      * [Connecting to Docker Server UGR](#connecting-to-docker-server-ugr)
      * [Connecting to Docker Containers](#connecting-to-docker-containers)
      * [Infrastructure](#infrastructure)
      * [Docker Cluster port assignment for VIRTUAL MACHINES](#on-docker-cluster-this-is-the-account-port-assignment)
      * [Hadoop Cluster port assignment for DOCKER CONTAINERS](#on-hadoop-cluster-this-is-the-account-port-assignment-for-docker-containers)

   * [2. Starting with OPENNEBULA](#starting-with-opennebula-and-openstack)
   * [3. Starting with DOCKER](#starting-with-docker)
   * [4. Starting with HDFS](#starting-with-hdfs)
   * [5. Starting with HADOOP](#starting-with-hadoop)
   * [6. Starting with SPARKR](#starting-with-sparkr)



# Environment of the practice

The working environment consists of the following structure for each user:

- 3 Clusters:
   - betatun.ugr.es
   - docker cluster  (15 nodes)
   - hadoop cluster  (15 nodes)

- betatun.ugr.es
   - Max 5 ports for docker containers.

- docker cluster provides for each user:
   - Max 1 Virtual machines (and 1 IPs)
   - Max 1 ports redirected from external to internal Virtual Machine network

- hadoop cluster provides for each user:   
   - BigData Software: Spark, Scala, SparkR, Hadoop, HDFS


![ClusterImage](https://sites.google.com/site/manuparra/home/clusterhadoop.jpg)

## Connecting to the clusters

Do you use Windows? Please install SSH Putty.

Do you use Linux or Mac? Fine!, nothing to do: use a Terminal (shell)


### Log in betatun ugr server with your credentials

```
ssh manuparra@betatun...
```

For this course use the next login credential:

- If your CardID number is spanish and similar to 77464888L,  your login will be: ``ssh CD_77464888@betatun....``
- If your CardID number is not spanish or you are using your passport similar to YM5664883L, your login will be: ``ssh CD_YM5664883@betatun......``

The  general rule is:
- Remove your last letter of your CardID number


After login, **PLEASE CHANGE** your password using command:

```
passwd
```

**Try to use a strong password mixing: upper, lower, and punctiation**



### Connecting to Hadoop Cluster UGR

Log in hadoop ugr server with your credentials (the same way):

```
ssh manuparra@hadoop...
```

For this course use the next login credential:

- If your CardID number is spanish and similar to 77464888L,  your login will be: ``ssh CD_77464888@hadoop....``
- If your CardID number is not spanish or you are using your passport similar to CD_YM5664883L, your login will be: ``ssh CD_YM5664883@hadoop......``

The  general rule is:
- Remove your last letter of your CardID number


After login, **PLEASE CHANGE** your password using command:

```
passwd
```


**Try to use a strong password mixing: upper, lower, and punctiation**


## Infrastructure

What is the infrastructure of the practice?

The complete infraestructure for the practice is the next:

![CompleteStruct](https://sites.google.com/site/manuparra/home/ArchitectureBDCC.png)


## Ports assignment betatun.ugr.es

Once connected to betatun, write:

```
cat puertosdocker.txt
```


# Starting with DOCKER

Go to: [First steps with Docker Containers](./starting_docker.md)

# Starting with OpenNebula and OpenStack

Go to: [First steps with OpenNebula](./starting_opennebula.md)
Go to: [First steps with OpenStack](./starting_openstack.md)

# Starting with HDFS

Go to: [First steps with HDFS]()

# Starting with Hadoop

Go to: [First steps with Hadoop]()

# Starting with SparkR (spanish)

Go to: [First steps with SparkR]()


