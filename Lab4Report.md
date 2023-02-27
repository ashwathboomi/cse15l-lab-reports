# CSE 15L: Lab 4 Report

### Step 1: Logging into ieng6 account

Entered `ssh cs15lwi23@ieng6.ucsd.edu` command into terminal 

![image](https://user-images.githubusercontent.com/113210547/221470597-c766dad5-0eba-4b81-87b5-ff5c70030da8.png)

As you can see, no password was needed to log into the account, speeding up the process

### Step 2: Cloning fork of repository

Entered `<CTRL + R> git <Enter>`. This resulted in `git clone git@github.com:ashwathboomi/lab7.git`

![image](https://user-images.githubusercontent.com/113210547/221471798-416eb6a2-e94e-4bf6-a336-f4fc326ba302.png)

This quickly cloned the repository into the ieng6 server.

### Step 3: Running the JUnit Tests

Entered `cd l<Tab>` to get `cd lab7/` and enter the directory

Entered `<CTRL + R> javac <Enter>` to get `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and compile all .java files

Entered `<CTRL + R> Test <Enter>` to get `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` and run JUnit Tests

This was the following output:

![image](https://user-images.githubusercontent.com/113210547/221472788-81919eef-1032-4971-9fed-a570fec28300.png)

There was one error with the merge method in ListExamples.java

### Step 4: Editing the code to fix the error

Since there is an error in Line 43 in ListExamples.java. I use the `<CTRL + R> sed <Enter` to get the `sed -i -e '43 s/index1/index2/' ListExamples.java`

![image](https://user-images.githubusercontent.com/113210547/221474440-57170e44-fc0e-4aad-b3f4-dfc656531b76.png)

### Step 5: Running the JUnit test to see if it passes now

Once again, I enter `<CTRL + R> javac <Enter>` to get `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and compile all .java files

and `<CTRl + R> Test <Enter>` to get `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

![image](https://user-images.githubusercontent.com/113210547/221474893-430c1949-12a7-4d70-b35f-f5025b6cf5e9.png)

We can see that ListExamples.java now passes both the tests in ListExamplesTests.java

### Step 6: Commiting and Pushing the code

Entered `git add ListExamples.java`, `git commit -m "added"`, and `git push`

![image](https://user-images.githubusercontent.com/113210547/221475439-8b682ac8-0c6a-401a-ad71-c6062d0d329c.png)

We can check the github repository on the web browser to see if it was updated recently after `git push`

![image](https://user-images.githubusercontent.com/113210547/221475597-2280557d-c8c2-432b-a6e4-054f0a79e8b7.png)

As you can see, it was updated 2 minutes ago, showing that our updates were successful.

