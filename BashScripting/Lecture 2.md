# Lecture 2

Bash space sensitive. ie ```(foo=bar)``` != ```(foo = bar)```  
First one assigns bar to foo whereas second one passes two arguments "=" and "bar" to function foo.  

Single quotes (') does not replace variables.
Double quotes (") replaces variable names.  
For eg:
```bash
echo "Value is $foo"
```
>Value is bar  
```bash
echo 'Value is $foo'
```
>Value is $foo  

A shell script file takes arguments with the name '$1' which is ismilar to 'argv' in other scripting languages. To execute a shell script (.sh), we have ```source FILE.sh```. If a function is present inside the script that requires an argument, it's passed as 
```FUNCTION_NAME ARGUMENT``` after the script is executed.

```$#``` is no. of arguments  
```$$``` is pid  
```$@``` all arguments
```$0``` is name of the script.  
```$1``` - ```$9``` is arguments it takes  
```$?``` will give error code with previous command.  
true has error code of 0 and false has 1
```$_``` will give last argument of previous command.  

```!!``` (bang bang) will replace the previous command.  
Eg:
```bash
mkdir /mnt/new
```
Permission denied
```
sudo !!
```
converts to ->
```bash
sudo mkdir /mnt/new
```

```echo $(pwd)``` $() substitutes the output of a command.

```grep``` searches for a substring in a file  

```touch foo{1,2,3,4}``` will expand as cartesian product as foo1 foo2 foo3 foo4  

