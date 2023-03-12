# CSE 15L Lab Report 5: Putting It All Together

## Using a Bash script to do Lab Report 4

### Cloning

After linking my GitHub account and my remote server acccount two weeks ago using ssh-keygen,
I was succesfully able to clone the lab 7 repository into the remove server using the command: `git clone git@github.com:ashwathboomi/lab7.git`
into my home repository on the remote server

![image](https://user-images.githubusercontent.com/113210547/224534432-e134138a-516c-4231-adf8-59ed65a5c963.png)

This was the first line of script that needed to be written


### Running JUnit Tests

The next step for the challenge was to run JUnit tests on ListExamples.java using ListExamplesTests.java

In order to do this, we first need to access the directory that contains both of these files, which is lab7

Since we are naturally in our home directory after we log in to the remote server, we include the command `cd lab7` in our bash script

We then proceed to compile all the files in the directory and run the tester file using the following command:

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

The .sh script should now look like this:

![image](https://user-images.githubusercontent.com/113210547/224535082-16b31e56-43dd-4799-a653-5c1952bdf99e.png)

### Modifying the file to Fix the Error

Using `vim ListExamples.java` to analyze the file beforehand, we can see that there is an error in line 42, where index1 variable should
be index2

Similar to how we fixed this before, we add `sed -i -e '43 s/index1/index2/' ListExamples.java` to our shell script.

Assuming we fixed our error, we will once again compile all the files within the lab7 directory and run the the tester file:

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

The script file should now look like this:

![image](https://user-images.githubusercontent.com/113210547/224535489-0896dfdb-9544-4339-b640-ec2d6a182272.png)

The expected output should now be that there is now no errors within ListExamples.java

### Pushing Updates

We can now add, commit, and push using the following commands:

`git add ListExamples.java`
`git commit -m "added"`
`git push`

The final script should look like this: 

![image](https://user-images.githubusercontent.com/113210547/224535675-11618c51-43dd-4a4e-9458-ac6090091a5e.png)

### Copying into Remote Server 

Since this file was created in local and we need to access it in our remote server to run all the script commands,
we use the command `scp script.sh cs15lwi23alj@ieng6.ucsd.edu:~` to copy the script into the home directory of 
our remote server.

![image](https://user-images.githubusercontent.com/113210547/224535814-c2d84038-5958-4491-a494-bc11e869b0fb.png)

### Running the Script File

To run the script, we go to the home directory and execute the command `bash script.sh`. The following output should occur:

![image](https://user-images.githubusercontent.com/113210547/224535956-3ae5af79-265e-4560-86eb-12a0144843fa.png)

### Completion

![image](https://user-images.githubusercontent.com/113210547/224534321-ffeb4f1a-25ea-40a6-9397-2014bf1f2e79.png)

The repository was succesfully updated as shown by the webpage.

Although writing the script took some time, the end product take almost 1 second to execute the same chain commands we needed to do
in Lab Report 4. The average taken before was around 30 seconds at best. This is a vast improvement. 

However, this was only possible because we knew all the commands to execute including the bugs in files. In the real world, this is rarely possible 
otherwise it would be easy to automate. Thus, this can only be used in certain specific scenarios.

