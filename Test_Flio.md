# Testing clearly work whith Instances

## Create a new Instances
1) On the main Navigation Panel go to `Cloud`, choose `Instances` and  click the plus `+` button from at the bottom-right of the screen.  

2) On the following page fill next information:
  - Instance Name 
  - Select a Boot source 
  - Select a configuration 
  - Select a SSH Key (try to generate new ssh key)

3) Hit `CREATE INSTANCE` button  

4) Wait untill status of your Instance will be *RUNNING*
When the VM has been created, you can view instance details. Take note of the *publicIpAddress*. This address is used to access the VM.

5) Try to access the VM using the folloving command:

```
ssh ip_address
```

6) Let's check, that we can clearly work in our Instance, try create a file (eg. file1.txt) and write some words into it (eg. start testing)

```
echo "start testing" > file1.txt
cat file1.txt
start testing
ls
file1.txt
```

## Create snapshot of your current instance:
1.  1) select your instance and click on **Snapshots tab**  
    2) click on the button `Create Snapshot`
    3) on the next page ензу the name of your new snapshot (eg. "test snapshot")
    4) click on the button `Create Snapshot` again  
2. Assume that we used our ability to copy (or snapshot)server successfully.
    1) continue to work in our Instance through the console,create a file (eg. file2.txt) and write some words into it (eg. continue testing)    

```
echo "continue testing" > file2.txt
cat file2.txt
start testing
ls
file1.txt file2.txt
```
So, we checked that we still can work with our Instance and now we have two our files  file1.txt” and “file2.txt”.

## Return to the previous state of Instance
1) click on the button `More` and choose `Rebuild` 
2) on the next page click `change` to change the boot source selected 
3) on the next page click `my images`, choose a snapshot which version of instanse you want to return and click `select`  
4) click `Rebuild Instance` and we returned to the previous state of our Instance  
5) check that we really return to the previous state of Instance 

```
ls
file1.txt 
```

## Resize the current instance:
1) go to Instances page, choose instance, which size you want to change
2) click on bottom more and choose action resize
3) choose new flavor of instance you need and click resize instance
4) wait until resize completed, login to your instance and confirm that the server is operational after resizing
5) choose Cofirm resize from the instanse menu to confirm migration was successful, otherwise choose Revert resize to revert back to the initial state.
6) check that our Instance is still working clearly -  create a file (eg. file3.txt) and write some words into it (eg. resize testing)    

```
echo "continue testing" > file2.txt
cat file3.txt
resize testing
ls
file1.txt file3.txt
```
## Delete instance
to delete an instance click the icon More and select Delete

