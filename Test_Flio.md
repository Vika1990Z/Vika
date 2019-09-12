# Testing clearly work whith Instances

1) **Create a new Instances**

* Access the VM using the folloving command:

```
ssh ip_address
```      
* Create a file (eg. file1.txt) and write some words into it (eg. start testing)

```
echo "start testing" > file1.txt
cat file1.txt
start testing
ls
file1.txt
```

2) **Create snapshot of your current instance:**

* Create a file (eg. file2.txt) and write some words into it (eg. continue testing)    

```
echo "continue testing" > file2.txt
cat file2.txt
start testing
ls
file1.txt file2.txt   
```   
* Restore from snapshot

```
ls
file1.txt 
```

3) **Resize the current instance:**
check that our Instance is still working clearly -  create a file (eg. file3.txt) and write some words into it (eg. resize testing)   

# Testing clearly work whith Clusters

1) **Create a new Cluster**
2) **Check that Cluster works clearly**
```
tail -f /var/log/cloud-init.log
kubectl get nodes 
kubectl get pods --all-namespaces
```

3) **Delete Cluster**
to delete a Cluster click the icon More and select Delete

