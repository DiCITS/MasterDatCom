# Hadoop Guide

Go to your HOME Folder:

```
cd WordCount
```

First: 

Copy ```textoulisesjoyce.txt``` to HDFS, to your ```HOME``` in ```HDFS```

```
hadoop fs -put textoulisesjoyce.txt textoulisesjoyce.txt
```

Compilation:

```
/usr/bin/javac -cp /usr/lib/hadoop/*:/usr/lib/hadoop-0.20-mapreduce/* -d wordcount_classes WordCount.java
```
Jar:
```
jar -cvf wordcount.jar -C wordcount_classes/ .
```
Execute:

```
# Example: hadoop jar wordcount.jar WordCount <input file HDFS> <output file HDFS>
```

```
hadoop jar wordcount.jar WordCount textoulisesjoyce.txt resultados_contar
```

Results:

```
hdfs dfs -ls resultados_contar
```

```
hdfs dfs -cat resultados_contar/part-00000
```

Merge Results:

```
hadoop fs -getmerge resultados_contar solucion.txt
```

# MIN HADOOP

```
cd 
```

then 

```
cd Min/
```

```
/usr/bin/javac -cp /usr/lib/hadoop/*:/usr/lib/hadoop-0.20-mapreduce/* -d minbigdata_classes Min.java MinMapper.java MinReducer.java 
```

```
jar -cvf min.jar -C minbigdata_classes/ .
```

```
hadoop jar min.jar oldapi.Min /tmp/ECBDL14_10tst.data salidamin
```





