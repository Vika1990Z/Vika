# Testing clearly work whith Instances

1. Create a new Instances

1.1 Access the VM using the folloving command:

```
ssh ip_address
```

1.2 Create a file (eg. file1.txt) and write some words into it (eg. start testing)

```
echo "start testing" > file1.txt
cat file1.txt
start testing
ls
file1.txt
```

2. Create snapshot of your current instance:

2.1 Create a file (eg. file2.txt) and write some words into it (eg. continue testing)    

```
echo "continue testing" > file2.txt
cat file2.txt
start testing
ls
file1.txt file2.txt
```
2.2 Restore from snapshot

```
ls
file1.txt 
```

3. Resize the current instance:
check that our Instance is still working clearly -  create a file (eg. file3.txt) and write some words into it (eg. resize testing)    

```
echo "continue testing" > file2.txt
cat file3.txt
resize testing
ls
file1.txt file3.txt
```
4. Delete instance
to delete an instance click the icon More and select Delete

