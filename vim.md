# Mastering Vim 
## Step 4 ##
![Logging into ieng6](images/step4.jpg)
In the image above, I am logging into ieng6. <br>
I am logging in from my home computer instead of my school laptop, <br> 
so I have to manually enter my credentials (no key-gen). <br>

Luckily, I have logged in before so I press the `<up>` key three times and hit `<Enter>` . <br>
My password saved on a sticky note is copied (`<ctrl>` + `c`) and pasted (by toggling `Edit` and clicking **Paste**). <br>

## Step 5 and 6 ##
![git clone](images/step5and6.jpg)
In the image above, two steps are shown. <br>

Step 5: <br>
**First I fork the repository from my GitHub account.** <br>
To do this, I press the `<up>` key 14 times <br>
then copied (`<ctrl>` + `c`) the url from my corresponding Github repository. <br>
I repositioned my cursor with the `<left arrow>` key so that I could get rid <br>
of the part between the domain and `/lab7` in the url. <br>
Hit `<backspace>` and entered `JackieGH` . <br>

Step 6: <br>
**Next, I run the tests demonstrating that they fail.** <br>
The first thing I do after cloning is enter `pwd` so that I know where I'm at. <br>
Followed by `ls` so that I can see what files exist in the current directory. <br>
I see the file I need, so I go into it by entering `cd l`, pressing `<tab>` to autofill <br>
the file name and once I am redirected I enter `ls` again. <br>
To run the preliminary test, I enter `bash` and `<tab>` to autofill the desired `bash test.sh` <br>

## Step 7 ##
![Editing with vim](images/step7.jpg)
Now that I know there is a bug in the `lab 7` files, I want to edit the file. <br>
So, I enter a series of commands and keys `vim`, `<shift>` + `L`, `<tab>` + `.` + `<tab>` <br>
to generate `vim ListExamples.java` to edit the file in vim <br>

I noticed that the cursor was positioned at the end bracket <br>
for `merge`, so I was able to navigate to the buggy line pretty quickly. <br>
While in normal mode, I hit the `K` key three times and the `L` key 10 times. <br>
Next, I hit `R` key followed by `2` key. This replaced the value without ever leaving normal mode. <br>
Lastly, I hit `:` followed by `wq` to prompt vim to save and exit.

## Step 8 ##
![git add](images/step8.jpg)
So, to get to this screen, I entered `git add --all` so that all changes of all files are staged to be committed. <br>
Next, I entered `git commit` . Since I didn't add `-m` to the end of the commit command, I was redirected to enter a **message**. <br>
I replaced the highlighted `#` with the message "test commit". To exit this screen I entered `:wq` for save and quit.

![git push](images/step8confirm.jpg)
It was all going well, at first. I entered `git push` and I was prompted to fill in my GitHub credentials. <br> 
However, I then got an error message because token codes replace passwords for pushing from a command line, <br>
so I had to leave the terminal to log into GitHub and enable tokens. <br>
Once I got the token code, I copied (`<ctrl>` + `c`) and pasted into the terminal (by toggling `Edit` and clicking **Paste**) in VSCODE. <br>
It went through and I got a successful push.

## Step 9 ##
![git push](images/steppush.jpg)
Upon checking with GitHub that I indeed pushed a change. Note the "test commit" message.
