https://www.youtube.com/watch?v=Z56Jmr9Z34Q&t=12s

```pwd``` Prints working Directory

```cd [PATH]``` Navigate

```cd -``` Toggle between current and previous directories

```cd ~``` Takes you to /home directory

```ls [OPTIONAL]``` Lists items in present directory

```ls *.exe``` Lists items with .exe extention  

```ls -l``` Long listing format  
- ```x``` : execute permission  
- ```r``` : read access  
- ```w``` : write access  

```ls -a``` Shows hidden files

```mv [FROM] [TO]``` Can move or even Rename the file

```cp [FROM] [TO]``` Copy file

```rm [PATH]``` Removes a file

```mkdir [NAME]``` Makes a dir in current directory

---

```< FILE``` Rewires the input stream from the file

```> FILE``` Rewires the output stream to the file

```>> FILE``` Appends to file

```cat [FILE]``` Preview a file

```[a] | [b]``` Pipe operator. This makes output from 'a' to be the input of 'b'.

---
$ ```sudo echo 500 > /sys/backlight/intel_backlight/brightness```
This will fail as brightness file is not opened as root.  
For root access : $ changes to # by the command ```sudo su```
  
Now,  
\# ```echo 500 > brightness``` will dim the lights

If not having root access, below would also work  
$ ```echo 1000 | sudo tee brightness``` as brightness is writing by superuser access. (```tee``` writes the output in file as well as terminal).   
```xdg-open [FILENAME]``` Opens a file in appropriate program.
