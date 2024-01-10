# cd: 
**no argument:**
```
[user@sahara ~]$ cd
[user@sahara ~]$
```
the working directory when the command was run was /home

since no argument is given to cd command, there is no directory to change to so we stay in the /home directory

the output is not an error 

**directory as argument:**
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```
the working directory when the command was run was /home

we gave the argument lecture1 to the command cd so we moved into the lecture1 directory

the output is not an error 

**file as argument:** 
```
[user@sahara ~/lecture1]$ cd Hello.java
bash: cd: Hello.java: Not a directory
```
the working directory when the command was run was /home/lecture1

since we used a file as an argument, we received an error because a file is not a directory

the output is an error because a file is not a directory 


# ls: 
**no argument:**
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
the working directory when the command was run was /home/lecture1

since no argument is given to ls command, the command will list all the files of the current directory

the output is not an error 

**directory as argument:**
```
[user@sahara ~/lecture1]$ ls messages
be.txt  en-us.txt  es-mx.txt  zh-cn.txt
```
the working directory when the command was run was /home/lecture1

since we used the messages directory as an argument for the ls command, the terminal listed all of the files present in the /home/lecture1/messages directory

the output is not an error 

**file as argument:**
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```
the working directory when the command was run was /home/lecture1

since we used a file as an argument for the ls command, the command simply reiterated the name of the file

the output is not an error 


# cat: 
**no argument:**
```
[user@sahara ~/lecture1]$ cat
^C
[user@sahara ~/lecture1]$
```
the working directory when the command was run was /home/lecture1

since no argument is given to cat command, the terminal concatenates nothing which causes the terminal to freeze. we can unfreeze the terminal by terminating the current process with ^C. 

the output is not an error

**directory as argument:**
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
```
the working directory when the command was run was /home/lecture1

since a directory is used as an argument for the cat command, we get an error message because a directory is not a readable file

the output is an error because cat cannot accept a directory as an argument 

**file as argument:**
```
[user@sahara ~/lecture1]$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}
```
the working directory when the command was run was /home/lecture1

since we used a file as an argument for the cat command, the terminal outputs the contents of the file

the output is not an error 
  
