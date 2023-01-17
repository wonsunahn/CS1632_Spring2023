- [Java Assessment Exercise](#java-assessment-exercise)
  * [Description](#description)
  * [Clone the GitHub Repository](#clone-the-github-repository)
  * [Install Apache Maven](#install-apache-maven)
  * [Install VSCode](#install-vscode)
  * [Install JDK 8](#install-jdk-8)
    + [Adding JDK 8 to PATH environment variable (Windows)](#adding-jdk-8-to-path-environment-variable-windows)
    + [Adding JDK 8 to PATH environment variable (MacOS / Linux)](#adding-jdk-8-to-path-environment-variable-macos--linux)
  * [Compile the Code](#compile-the-code)
  * [Run the Code](#run-the-code)
  * [Complete SortedCollection.java](#complete-sortedcollectionjava)
  * [Test the Code](#test-the-code)
  * [Submission](#submission)
  * [GradeScope Feedback](#gradescope-feedback)
  * [Resources](#resources)

# Java Assessment Exercise

DUE: January 17 (Tuesday), 2023 Before Class

Please accept Exercise 0 on **GitHub Classroom** using the following link:
https://classroom.github.com/a/RplfE52v

When you accept the assignment, a new GitHub repository will be automatically
created for you with which you will do backup, versioning, and even submission.
If you are new to git versioning, please read the section [Clone the GitHub
Repository](#clone-the-github-repository) extra carefully.

## Description

The purpose of this exercise is to assess your Java programming skills coming
to this class.  On your GradeScope feedback, I may recommend that some of you
drop the course if your programming skills are not up to par.  Credit will be
given for participation but the actual score will not count towards the final
grade.

Another purpose of this exercise is to familiarize you with the workflow for
this course.  We are going to use GitHub for collaboration and source code
versioning, and also for submitting to GradeScope.  Once your code is submitted
to GradeSCope, the autograder will automatically test your code and assign a
score depending upon the pass/fail of each test case.  The autograder will also
give you valuable feedback on the deductions you got so that you can fix your
mistakes and resubmit to get a higher score.  There is no limit to the number
of submissions.

Please follow the below instructions.

## Clone the GitHub Repository

For every source code submission in this class, you are asked to create a new
GitHub repository.  Git is one of the most popular source versioning and
collaboration tools used in industry and GitHub is a major provider of that
service.  If you don't already have a GitHub account, please create one.  If
you are new to GitHub, there is a short git tutorial under the lectures folder:
[Using_Git.pdf](/lectures/Using_Git.pdf).  Please refer to it as you follow the
below instructions.

1. If you are new to git source versioning or GitHub, I recommend that you
start by using the Desktop GUI version.  You can download it from:

2. Once you've installed GitHub Desktop, let's first clone the Exercise 0 GitHub repository to your computer:

   https://help.github.com/en/desktop/contributing-to-projects/cloning-a-repository-from-github-to-github-desktop

   Please clone the GitHub Classroom repository that was created for you when you accept the assignment to your desktop.

   Whenever there are updates to the GitHub Classroom repository (for example,
somebody did a "Push" to the repository), the "Pull" request button will be
activated for the repository on GitHub Desktop.  Clicking that button will
bring your Local Repository in sync with the Remote Repository at GitHub.com.

3. Whenever you make improvements to your source code, frequently "Commit" and
   "Push" those changes to GitHub so that your new changes are versioned.

   Committing your changes will transfer the changes from the source code that
you are working on to the Local Repository creating a new version.  Pushing
your changes will upload new versions in your Local Repository to the central
Remote Repository at GitHub.com.  So only after you Push will the changes be
available to your collaborator to Pull (or yourself from a different machine).
Committing and Pushing frequently ensures that your changes are versioned and
backed up, as well as allowing your collaborators to access your changes and
keep up-to-date.

For more details about using Git and GitHub, please refer to the following tutorial:
https://classroom.github.com/a/DWR7V_Np

Clicking on the above link and accepting the assignment will create a new
GitHub repository for you with the tutorial.  Completing the tutorial is
optional but is recommended for first time Git users.  You can play around with
this new repository until you get used to Git operations, without having to
worry about deleting or overwriting important source code.

Also optionally, you may decide to clone the course repository at
https://github.com/wonsunahn/CS1632_Spring2023 to your desktop as well.  Since
you don't own this repository, you will have to choose the "URL" tab when
cloning and input that URL.  Also, you will only be able to Pull from the
repository and not Push.  But if you want to have access to course materials
while offline, that is a great option.  If you do this, please make sure that
you click on "Fetch Origin" on GitHub Desktop and Pull any changes frequently
(before every class) to keep up-to-date with newly released materials.
 
## Install Apache Maven

In this class, we will be using the Apache Maven build framework to build and
test our code.  Please download the binary zip file from:
https://maven.apache.org/download.cgi

Unzip the file at your preferred location and add the bin directory to your PATH enviornment variable as instructed in:
https://maven.apache.org/install.html

## Install VSCode

In this class, we will be using VSCode as our default IDE.  It makes
collaboration, code sharing, and other tasks much easier.  You may use other
IDEs if you choose to do so.  All exercises and deliverables are designed so
that they can be done independent of an IDE.

If you choose to use VSCode, please download and install:
https://code.visualstudio.com/download

Please also install the "Extension Pack for Java" on VSCode by searching for it on the Extensions menu:
https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack

You may also want to familiarize yourself with the Live Share in preparation of working with a partner:
https://code.visualstudio.com/learn/collaboration/live-share

## Install JDK 8

The official Java version for this class is Adoptium Temurin JDK 8
(1.8.0_352).  It is **very important that you install JDK 8** because some
testing tools we will use in this class may not be compatible with other
versions of Java.  You can easily install the JDK using VSCode by following
these steps:

1. Click on View > Command Palette.  This will launch the command palette at
   the top part of the IDE.
2. Search for "Java: Install New JDK" on the command palette.  This will
   create a new tab named "Install New JDK".
3. Click on the 8(LTS) version and then the "Download" button.
4. Launch the downloaded JDK installation package and go through the steps.
5. Click on the "Reload Window" button on VSCode as instructed.

### Adding JDK 8 to PATH environment variable (Windows)

For Windows, the installation package should automatically update the PATH
variable so you don't need to do anything extra.  If you query the Java
version on the "Terminal" tab on VSCode or on a regular CMD terminal on
Windows:

```
java -version
```

You should get the following:

```
openjdk version "1.8.0_352"
OpenJDK Runtime Environment (Temurin)(build 1.8.0_352-b08)
OpenJDK 64-Bit Server VM (Temurin)(build 25.352-b08, mixed mode)
```

If you don't see the correct version, please follow the below instructions
to set up the PATH OS environment variable.

1. Search "environment" in the Windows 10 search box.
2. Open "Edit the system environment variables" control panel.
3. Click on the "Environment Variables" box.
4. Search the "PATH" environment variable in user variables and system variables.
5. Add the bin directory of the Java installation, probably "C:\Program Files\Eclipse Adoptium\jdk-8.0.352.8-hotspot\bin" to the top of the "PATH".
6. For good measure, you may want to remove other Java installations from the "PATH".
7. After this, try doing "java -version" again on a new terminal and it should have changed.

### Adding JDK 8 to PATH environment variable (MacOS / Linux)

Below instructions are assuming you are using the bash shell.  If you are
using the zsh shell instead of the bash shell, please modify ~/.zshrc
instead of ~/.bash_profile.  You can see what shell you are using by doing
"ps" on the commandline. 

1. Open ~/.bash_profile with your favorite editor (if you don't have one, just do "pico ~/.bash_profile")
2. Add the following 2 lines at the bottom
   ```
   export PATH=/Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home/bin:$PATH
   export JAVA_HOME=/Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home/
   ```
3. Save the file and exit from the terminal
4. Relaunch the terminal and try doing "which java".  It should say "/Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home/bin/java".
5. Now you are good to go!  Otherwise, try doing "echo $PATH" and see if your path is not updated properly, or if there is some other Java installation before you.


Alternatively, you can use [jEnv](https://www.jenv.be/) that allows you to
switch Java versions easily on a Mac.  You will also need [Mac
brew](https://brew.sh/) if you don't already have it.  It's a brew
installation so it should be pretty painless.

## Compile the Code

If you are working on the VSCode IDE, it will auto-compile the code
everytime you make a change.  If you have issues, they will show up on the
"Problems" tab at the bottom pane.

If you feel the need to manually compile on the
commandline, you can use Apache Maven:

```
mvn compile
```

We will have an opportunity to talk more about Maven later on, so don't
worry if you are unfamiliar with it.

## Run the Code

You can run the main method of SortedCollection by using the VSCode "Run and
Debug" menu on VSCode: https://code.visualstudio.com/docs/editor/debugging.

Once you press "Launch SortedCollection", you will get prompted for
arguments to pass to the program, which is the list of numbers to sort.  For
example, if you pass "3 2 1", you will get the output:

```
sorted: 0 0 0
```

That is because SortedCollection.java is as of now incomplete.  Once you are
done, you should get the correct output:

```
sorted: 1 2 3
```

Again, you can also run the class using Apache Maven on the terminal.

On MacOS / Linux:

```
mvn exec:java -D"exec.args=3 2 1"
```

On Windows:

```
mvn exec:java -Dexec.args="3 2 1"
```

Currently, it shows an output that looks like the below:

```
...
[INFO] --- exec-maven-plugin:3.0.0:java (default-cli) @ sortedcollection ---
sorted: 0 0 0 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
...
```

if you run the program without arguments, it just shows the usage info:

```
mvn exec:java
```

```
...
[INFO] --- exec-maven-plugin:3.0.0:java (default-cli) @ sortedcollection ---
Usage: java SortedCollection [num1] [num2] [num3] ...
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
...
```

Your job is to complete SortedCollection so that it works properly.

## Complete SortedCollection.java

The places in source code where you are asked to insert or modify code are
marked by // TODO comments.  Feel free to use any data structure from java.util
or one of your own.  It doesn't matter how you implement it as long as it works
as specified.  Pay attention to the Javadoc comments on top of each method.

## Test the Code

I have written a test class to test your SortedCollection implementation
named SortedCollectionTest under the src/test folder.  You can use the
VSCode "Testing" menu to run the test:
https://code.visualstudio.com/docs/java/java-testing.

Or, again, you can use Apache Maven instead:

```
mvn test
```

Initially, most of the tests will fail:


```
...
Tests run: 10, Failures: 9, Errors: 0, Skipped: 0

[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
...
```

When you are done with implementing SortedCollection, all the tests should
pass.  If they don't try reading the failing test to understand what you did
wrong.

## Submission

When all tests pass, you are ready to submit.  Please submit your GitHub
Classroom repository to GradeScope at the "Java Assessment Exercise" link.
Once you submit, GradeScope will run the autograder to grade you and give
feedback.  If you get deductions, fix your code based on the feedback and
resubmit.  Repeat until you don't get deductions.  

Don't forget that you have to
Push your changes to upload them to the repository.

IMPORTANT: Please keep the github private!  This applies to all future submissions.

## GradeScope Feedback

GradeScope feedback is your friend.  Submit as many times as you want to get
frequent feedback.  There are 10 tests for this exercise and if there is an
error, the error message will tell you what was expected what was observed.
When the compared value is a string, brackets ([, ]) are used to annotate
exactly which part of the two strings differed.  If all the
SortedCollectionTest tests passed, then you should not get any deductions
because GradeScope runs the exact same tests.  

## Resources

* Java 8 API reference manual:
https://docs.oracle.com/javase/8/docs/api/overview-summary.html
