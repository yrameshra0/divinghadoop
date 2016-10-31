# Diving into learning Hadoop with its contructs.

## Installing Hadoop
Getting started with downloading stable distribution of hadoop from this [link](http://mirror.fibergrid.in/apache/hadoop/common/stable/hadoop-2.7.3.tar.gz).

## Configuring for Psuedo-Distributed mode using **localhost**

On OS X please make sure that we can *ssh localhost* without requiring a password. If password is prompted then the below mentioned steps have to be followed

Check if you have already generated key for using it at some other source. If you have **id_rsa.pub** available at **~/.ssh/**, in which case do the following

``` 
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```
If no keys are available the we should generate one using
```
ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```

With this you should be able to use 
```
ssh localhost
``` 
Without requiring to enter any password



