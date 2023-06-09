# Debugging!
## the original post
![ogpost](images/post1.png)
![second half](images/post2.png)

## the TA response
![ta](images/ta.png)

## the resolution
![fixed code](images/passed.png)
![fixed](images/fixed.png)

## the setup
The file and directory structure needed to replicate this scenario can only be replicated by <br>
Cloning the lab7 repository from CSE15l lab from the command-line in a terminal <br>
Then you will want to change directory into `lab7` <br>
Next, you will need to do `bash test.sh ListExamplesTests.java` from the command-line <br>
to compile and run the file so you can see what tests you passed or failed <br>
You should get a pass with 2/2 but to replicate the student's mistake you need to change the expected <br>
array to the way it is shown in the screenshot <br>
Adding a `c` element to correctly reflect the missing element once merged should fix the problem <br>
Run `bash test.sh ListExamplesTests.java` again and you should pass all tests again.
