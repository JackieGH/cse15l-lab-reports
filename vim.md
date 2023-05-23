# Mastering Vim 
## Step 4 ##
![Logging into ieng6](images/step4.jpg)
In the image above, I am logging into ieng6. <br>
I am logging in from my home computer <br>
instead of my school laptop, so I have to manually <br> 
enter my credentials (no key-gen). <br>
Luckily, I have logged in before so I press <br>
the `<up>` key three times and hit `<Enter>` . <br>
My password is saved on a sticky note so I copy (`<ctrl>` + `c`) <br>
and paste (by toggling `Edit` and clicking **Paste**) into VSCODE. <br>

## Step 5 and 6 ##
![git clone](images/step5and6.jpg)
In the image above, two steps are shown. <br>
Step 5: <br>
**First I fork of the repository from my Github account.** <br>
To do this, I press the `<up>` key 14 times (I know, not very efficient) <br>
then copied (`<ctrl>` + `c`) the url from my corresponding Github repository. <br>
I repositioned my cursor with the `<left arrow>` key so that I could get rid <br>
the part between the domain and `/lab7` in the url. Hit `<backspace>` and <br>
entered `JackieGH` .
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
So, I enter `vim`, `<shift>` + `L`, `<tab>` + `.` + `<tab>` <br>
Don't be alarmed, it's only the input to generate `vim ListExamples.java` so that we can edit the file in vim <br>
I noticed that the cursor was positioned at the end bracket for `merge`, so I was able to navigate to the buggy <br>
line pretty quickly. While in normal mode, I hit the `K` key three times and the `L` key 10 times. <br>
Next, I hit `R` key followed by the number `2` key -- this replaced the value 1 with 2 without ever leaving normal mode. <br>
Lastly, I hit `:` followed by `wq` to prompt vim to save and exit.

## Step 8 ##
![git add](images/step8.jpg)
So 
![git push](images/step8confirm.jpg)
## Step 9 ##
![git push](images/steppush.jpg)
