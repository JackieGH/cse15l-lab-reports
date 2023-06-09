# Connecting to a Remote Server #
 
*5 minute read, 30-90 minute setup* 

In this tutorial, we are going to learn how to (legally) hack into a remote server from our computer and gain access to its files!<br>
We will be using VSCODE and our course-specific account to connect to UCSD computers.

### Part 1 : Finding Course-Specific Credentials ###
Before doing anything we need to know the username and password associated with the account we want to access.

Start by visiting this link for [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
<img src="./images/accountlookup.png">

Login with your student ID and student username. <br>
Note: Your username corresponds to the first part of your student email before the "@" <br> (i.e `student1` is the username for student1@ucsd.edu)

<img src="./images/resultsloggedin1.png">

Once logged in, you should see a page titled **Account Lookup Results** navigate to the **Additional Accounts** section.<br>
Depending on your course history there may be several buttons to choose from.<br>
**Click** the account button relevant to this course, it should start with `cs15lsp23__` <br>
(Replace the blank with the last two letters assigned to your username.)

You should now be on a page that looks very similar to the previous page. <br> Your course-specific username should be the first thing under **Account Lookup Results**. <br> You should also see a warning box prompting you to set your account password. <br> Click the blue link titled <ins>Global Password Change Tool</ins> 

<img src="./images/resultsloggedin2.png">

#
This is important--once redirected, make sure to enter your course-specific username, **NOT your general student username** or you will reset your AD password. 
Be Prepared To Wait: Resetting the password requires a minimum of 15-60 min before a successful login.

<img src="./images/enteruser.png">


*If VSCODE is already downloaded onto your computer, wait at least 15 min before moving onto **Part 3**.* <br>
*If you do not have VSCODE downloaded continue to **Part 2**.*
#

### Part 2: Downloading VSCODE ###
Visual Studio Code is a code editor and you will use its terminal to connect to a remote computer. An internet connection is necessary. 

Go to the [Visual Studio Code site](https://code.visualstudio.com/)

Download the version that corresponds to your operating system and open the editor. <br>
Tip: On Mac, make sure to move VSCODE out of your Downloads folder and into your Apps Folder if you can’t find it in Spotlight.

VSCODE should look something like this:
<img src="./images/VSCODE.png">

### Part 3: Remotely Connecting ###
*Reminder: Make sure you waited at least 15 minutes to let the password set before starting this section.*

The hardest part is already past us!

Next, copy the following command in VSCODE terminal, don't forget to fill in the last two letters of your username.
Enter `ssh cs15lsp23__@ieng6.ucsd.edu`
Note: Use copy and paste when prompted to enter the password. It will be invisible to you with no sign that even the curser has moved--this is normal.

If you run into a question about authenticity and connecting? Enter `yes`, this is also normal since it should be your first time connecting to the server.

<img src ="./images/firsttimelogin.png">

If all the credentials were correct, you should now be virtually connected to another computer!
<img src ="./images/success.png">

If you are having trouble connecting, consider waiting out the maximum time. <br> Then, if you are still having trouble connecting, revisit the <ins>Global Password Change Tool</ins> and reset your course-specific password again. Repeat **Part 3**.

### Part 4: Trying Some Commands ###
The first command you should try in your terminal, should always be `pwd` since it will let you know what directory you are in.
Other notable commands include: <br>
`ls` which will show you a printout of all the files in your current directory. <br>
`cd` which stands for change directory and will be useful when you need to move into another folder. <br>
`mv` to move a file into another directory. <br>
`cp` to make a copy of a file. <br>
`rmdir` to delete a folder that you made on accident or no longer need. <br>
`clear` my favorite: clears your terminal of all the commands you ran. <br>
Bonus: Not technically a command but extremely useful is the up-arrow key. Click it once or twice and it will start cyling through previous commands so you won't have to type them again.


Review the following screenshots to see what these and other commands can do:
<img src="./images/somecommands.png">
