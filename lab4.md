# Lab Report 4: Vim

### Log into ieng6
input: `ssh drcano@ieng6.ucsd.edu`

output: ![Image](sshss.jpg)

comments: we use the secure shell protocol to connect to our student account on the `ieng6.uscd.edu` server 

### Clone your fork of the repository from your Github account (using the SSH URL) 
input: `git clone git@github.com:drcano/lab7.git`

output: ![Image](gitclone.jpg)

comments: after forking the repository, we can clone the repositiory from our github account using the `git clone` command and entering the repositiory url. 

### Run the tests, demonstrating that they fail
input: `cd lab7` -> `bash test.sh`

output: ![Image](testfail.jpg)

comments: For this process, the `ieng6-203` server didn't allow the `javac` command to be ran so I exited and reconnected to the `ieng6-201` server so that the jUnit tests could finally compile and still fail. To run our jUnit tests, I entered the `lab7` directory created by the `git clone` command using the command `cd lab7` and then used the `test.sh` file to run the jUnit tests with the command `bash test.sh`

### Edit the code file to fix the failing test
input: `vim ListExamples.java` -> `/index1` -> `<n>` (x9) -> `<e>` -> `<r>` -> `2` -> `:wq!`

output: ![Image](vim.jpg)

comments: To edit the code, I used the `vim` command to enter the text editor and searched for index1, using `/index1` command, until I found the error in the code. I replaced index1 with index2 to fix the error using the `<r>` command in vim and saved the changes to the file and quit vim using the command `:wq!`

### Run the tests, demonstrating that they now succeed
input: `<up><up><enter>` 

output: ![Image](testpass.jpg)

comments: Since I already ran the `bash test.sh` command earlier, I simply hit the `<up>` key twice to recall the command from bash history and hit `<enter>` to run the command. 

### Commit and push the resulting change to your Github account

input: `git commit -am "new update"` -> `git push` 

output: ![Image](gitpush.jpg)


comments: To solidfy the changes to the main repository on github, I committed the changes from my local machine using the command `git commit -am "new update"`, the `-a` option allows us to skip the `git add` command and go straight to committing the changes from our local directory to the main github repository. After the changes are committed, we can push the changes to the main github repository branch using the `git push` command and our main github repository is fully updated with the changes that we made on our local machine. We can use the `git log` command to see the author, date, and message for the commit that was made.  
