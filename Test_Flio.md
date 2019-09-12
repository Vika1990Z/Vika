# Testing clearly work whith Instances

## Create a new Instances

### Access the VM using the folloving command:

```
ssh ip_address
```

### Create a file (eg. file1.txt) and write some words into it (eg. start testing)

```
echo "start testing" > file1.txt
cat file1.txt
start testing
ls
file1.txt
```

## Create snapshot of your current instance:

### Create a file (eg. file2.txt) and write some words into it (eg. continue testing)    

```
echo "continue testing" > file2.txt
cat file2.txt
start testing
ls
file1.txt file2.txt
```
### Return to the previous state of Instance

```
ls
file1.txt 
```

## Resize the current instance:
check that our Instance is still working clearly -  create a file (eg. file3.txt) and write some words into it (eg. resize testing)    

```
echo "continue testing" > file2.txt
cat file3.txt
resize testing
ls
file1.txt file3.txt
```
## Delete instance
to delete an instance click the icon More and select Delete

