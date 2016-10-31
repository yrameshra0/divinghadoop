# Diving into learning Hadoop with its contructs.

## Installing Hadoop
Getting started with downloading stable distribution of hadoop from this [link](http://mirror.fibergrid.in/apache/hadoop/common/stable/hadoop-2.7.3.tar.gz).

## Configuring for Psuedo-Distributed mode using **localhost**
Followed setups mentioned [here](http://hadoop.apache.org/docs/r2.7.3/hadoop-project-dist/hadoop-common/SingleCluster.html#Pseudo-Distributed_Operation)

*Caveats, required for my personal setup*
### Configuring SSH
On OS X please make sure that we can *ssh localhost* without requiring a password. If password is prompted then the below mentioned steps have to be followed

Check if you have already generated key for using it at some other source. If you have **id_rsa.pub** available at **~/.ssh/**, in which case do the following

``` 
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```
With this you should be able to use 
```
ssh localhost
``` 
Without requiring to enter any password

### Configuring Sites

I created separate pseudo distributed configurations [here](https://github.com/yrameshra0/divinghadoop/tree/master/hadoop/pesudo-distributed-configs) with this 
configurations there was no mention that **capacity-scheduler.xml** is required too but **resource-manager** instance was failing instantiation and reason was non-occurrence of this file. 


