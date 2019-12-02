# GitHub Tutorial

_by Alana Liu_

---
## Git vs. GitHub
**Git**
* Allows you to manage and keep track of your code
    * Version control system
        * keep “snapshot” of code
    * Allows you to undo a previous version

**Github**
* Stores info in cloud
    * Allows you to manage Git repository
    * Visually tracks changes
* Easily collaborated


---
## Initial Setup

1. Go to [github.com](https://github.com/)
2. Press Sign Up
3. Enter a Username (If you're an HSTAT student this should be your firstname_lastname_last4osis#)
4. Enter an Email (If you're an HSTAT student please enter your email associated with the school)
5. Enter a password (If you're an HSTAT student your password could be your osis#)
6. Now click the green button _(Sign up for Github)_
7. **DO NOT FORGET TO VERIFY YOUR EMAIL**

CONGRATULATIONS YOU NOW HAVE A GITHUB ACCOUNT!!!!

> Now let's set up your ide. Please click the link below and follow the steps **SLOWLY & CAREFULLY**

[github.com/hstatsep/ide50](https://github.com/hstatsep/ide50)
> In this link you are going to be introduced to an **SSH key.** The steps you're following in the link above is connecting you're GitHub account with your ide. This will make it easier for you to upload your projects into Github (remote) without having the need to sign in everytime.
---
## Repository Setup
> Now that you have set up your ide and your Github account you can now create repositories.

1. Go to the directory you desire to turn into a repository
2. Type `git init` in the command line
3. Now you need to create a file that you can edit and make changes to
    * In the command line type `touch <filename>`
4. Once you've made the file type `c9 <filename>` to open the new file
5. In this file you can type anything you want
6. Once you're done making edits in the file go back to the command line and type `git add .`
7. Now still in the command line type `git commit -m "short/specific message"`
    * The short/specific message should be in the present tense and also describe what you change you did in the file.
8. Once you have committed (saved the changes) you can now go back and do some more edits in the file.
9. Now repeat:
    * Edit your file, add it and commit it


---
## Workflow & Commands
> You've just used `git init` , `git add` & `git commit` but you really don't know what they exactly do. Bellow is a list of commands you have already used and commands you haven't used that will come in handy.

REMEMBER **ALL** these commands are typed in the command line:

`git init` - This command initializes the git in a directory
* If git is initialized in a directory its now called a repository.
    * Do it in directory that you want to turn into repository
    * DO NOT DO IT IN ROOT DIRECTORY

        * `rm -rf .git` - If you ever initialize git in the wrong directory or in the root directory just type this command and it will uninitialize git.

> The following two commands are used when you are done making edits in the file and you want to add them to the stage. Adding them to the stage allows you to save them later on.

`git add file.ext` - Adds changes for a *specific file* to the stage ready to commit

`git add .` - Adds changes of **ALL** files to the stage

`git status` - Ever wonder if you have added a file to the stage ready to commit. Well git status allows you to see what you have added or no.
> If you see `Modified: <file_name>` in red, it means you haven't added it to the stage. While if you see the same text in green it means its been added to the stage and its ready to be committed.

`git commit -m "short/specific message"` -  Use this command when you are done adding your edits and are ready to be committed (saved).
* Your message *must be:*
    * In present tense
    * Short
    * Specific
    * Describe the change you did in the file

> These commands above are probably the commands you're going to be using the most. On the other hand, the following two commands are mostly optional and are used in the event you want to see previous commits.


`git diff` - If you ever want to see the difference between  your current edit and the previous commit this will do the job.

`git log` - You may also just want to see your previous commits. Well in that case, this commit will display **ALL** previous commits you've done.
* Press *Control* and the *letter q* on the keyboard to get out of `git log`

#### Setting up Push and Pull

> Pushing and Pulling are very important once you begin having a local repo and a remote repo. Bellow is a brief explanation of what they both do and how to use them.

`git push` - Send commits from local repo (ide) “up” to remote repo (github). Its like updating your local.

> Before using this commands we will have to set where the commits will go. In other words we have to set where we are pushing it. This will require some steps but after them you will be able to use both commands above.

1. Create a repository by initializing git in a directory.
2. Make a file called README.md
3. Once you've done the steps above go to [github.com](https://github.com/) and sign in.
4. Click on the _plus icon_ located on the top right side of your screen
5. Now click on *create repository*
6. Enter the name of your repository from your ide
    * This has to be identical or else it wont work
7. Scroll down and make sure you have "Initialize this repository with a README" **OFF**.
8. Click the green button _"Create Repository"_
    * This will direct you to another page
9. You will see code similar to this
    * If you dont make sure SSH key is turned on
```
git remote add origin git@github.com:user_name/repository_name.git
git push -u origin master
```
10. Copy the code from **YOUR** page and paste it in the command line
11. Press enter

* Now when you edit your README.md add it & commit it, you can now use just the command `git push`

> What you just did was program your ide where to upload your repository in the cloud. If you didn't select SSH key you would have to be signing in every time you are going to push and pull. If you didn't use SSH and instead used HTTPS you will have to sign in to push or pull. Some of you may be wondering why you don't have to sign in when you use the SSH key. Well earlier when you set up your ide with yout github, you linked them together and so the computer is smart enough to recognize this and wont ask for your information again.

* Let's explain what the commands you put in the command line did.
    * `git remote add origin URL` - In simple words is setting up the connection between the local repo and remote repo.
    * `git push -u origin master` - The command creates a permanent bridge between the remote and the local. This allows to push without the extra origin master part that usually follows the command.

`git remote -v` - Ever want to remind yourself where the commits are being sent. Just type this and it will tell you where you can pull and push. This is similar to `git status`

> On the other hand `git pull` doesn't require extra steps to be able to use it. You would use this command only if you're working straight off your remote repo (Github) and wanted to update your local.

`git pull` - Sends commits from remote repo (github) down to local repo (ide). Its like updating your remote.

#### Cloning Vs Forking

##### Clone:

> Right above, you just learned how to back up your local repo. In the event of you local repo disappears due to a virus, accidental deletion or want to work off someones project for yourself, cloning can come in real handy. Follow the steps below to learn how to clone.

1. Go to [github.com](https://github.com/)
2. Go to the repository you'd like to acquire
3. Click on "Clone or Download"
    * Make sure it says "Clone with SSH"
        * If it says "Clone with HTTPS" click "Use SSH"
4. Copy the URL
5. Go to your ide and make sure you are in the directory where you want this repo to go
6. Type `git clone` and paste the URL after it
7. Press enter
    * If you are going to work in the repository make sure to `cd` into it.

`git clone` - Allows you to copy a remote repo into your ide.

> Unfortunately with `git clone` you can not push your local commits to the remote repo. This is because when you clone you have a local copy of **THEIR** remote repo. To add on, You do not have permission to push to their remote. This is where forking comes in.

##### Collaboration 

**Forking**

> Forking on the other hand, give you a **remote copy** of *THEIR* **remote repo**. You can then clone your remote to your local machine. You do have permission to push to your remote. Keep in mind in order to fork you need to know how to clone. Down bellow is a guide on how to Fork.

1. Go to [github.com](https://github.com/)
2. Go to a repository you'd like to fork
3. Click on the fork button located at the top right of the screen.
4. Once it finishes loading click on "Clone or Download"
    * Make sure it says "Clone with SSH"
        * If it says "Clone with HTTPS" click "Use SSH"
4. Copy the URL
5. Go to your ide and make sure you are in the directory where you want this repo to go
6. Type `git clone` and paste the URL after it
7. Press enter

> Now you can work on the local repository and then push it the remote repository. Forking is amazing when you are trying to collaborate with others or even trying to suggest changes in the remote repo. If you want to learn how to suggest changes to the owner of the original remote repo follow the steps below. 

**Send and Accept Pull Request**


1. Follow the steps on how to fork 
2. Make a change in the file of the local repo that was just formed by forking and cloning. 
3. After the change/edit 
    * `git add` 
    * `git commit -m "specific/short change`
    * `git push`
        * ***VERY IMPORTANT TO DO THESE STEPS***

> Some of you may be like, but wait don't we have to go through the procedure of setting push up? Well no because when you forked and clone you at the same time set the location where you're going to push.

6. Go to the owners version of the repository 
7. Click on _"New pull request"_
    * Github is smart enough to compare their remote repo with your remote repo
8. Now click on _"Create pull request"_
9. Write a comment saying why they should make the revisions and use yours instead.
10. Click on _"create pull request"_

> Keep in mind what you're suggesting to change is based on the commits and what you pushed to your remote repo. Once you send a pull request they will get notified through their email and you just have to wait to see if they accept the changes. In the end it's the owners decision to change it or not.

If you're the owner and want to figure out how to accept/merge the pull request, follow the steps below to figure it out.

1. Go to your remote repository that received a pull request
    * You can quickly access this by going to the email you got with the pull request and click the first link given 
2. Click on pull request    
    * Located in between _"Issues"_ and _"Actions"_
3. Open the pull request that was sent by someone 
4. If you desire to accept the changes after viewing them CAREFULLY click "Merge pull request"
5. Click _"Confirm Merge"_
6. Check the remote repo and make sure it went through

 > You may think you're all done because it's there in your remote repo but if you look carefully in the local remote it's not there. Some of you are going, well how do I get it there then? Well this is where `git pull` comes handy.
 
7. Go to your local repo 
8. In your command line type `git pull`
    * This updates your local repo by fetching the information located in the remote repo

> CONGRATULATIONS!!!! You're all done, you now know how to send pull requests and even accept them if you ever get one. 

---
## Rolling Back Changes

> Everyone makes mistakes and in coding it's definitely bound to happen. The important things to keep in mind is how to undo them. Below are lists of commands that will help you undo them in the case of a mistake or  you just changed your mind.

`git checkout -- file` - After you edited your file you may change your mind and prefer the previous version over your current one. This is where this command come into use since it will "unedit" you current file.

`git reset HEAD file` - When you accidentally or change your mind over a file you added to the stage you can  "unadd" by using this command.
* In the event you forget this command, you see it by typing `git status` 

`git reset --soft HEAD file` - Sometimes you may want uncommit and this is where this command comes into use.
> The commands above only undo commits, what you've added and edited one by one. If you want to save a little more time the following commands will undo multiple at the same time.

`git reset HEAD~1` - This command will undo what you added and the commit and take you directly to the editing phase.

`git reset --hard HEAD file` - Ever want to just go all the way back before commiting, adding and even having any edits done. Well this command will take you all the way back.

> Before learning the next command you need to know each commit has it own unique SHA code. This could be accessed by doing `git log`

`git reset --hard [first nine digit of SHA]`- This command erases the commit you made from your remote. In other words this is _"Unpushing"_ a file.





