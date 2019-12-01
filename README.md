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
3. Enter an Username (If you're an HSTAT student this should be your firstname_lastname_last4osis#)
4. Enter an Email (If you're an HSTAT student please enter your email associated with the school)
5. Enter a password (If you're an HSTAT student your password could be your osis#)
6. Now click the green button _(Sign up for Github)_
7. **DO NOT FORGET TO VERIFY YOUR EMAIL**

CONGRATULATIONS YOU NOW HAVE A GITHUB ACCOUNT!!!!

> Now lets set up your ide. Please click the link bellow and follow the steps **SLOWLY & CAREFULLY**

[github.com/hstatsep/ide50](https://github.com/hstatsep/ide50)
> In this link you are going to be introduced to a **SSH key.** The steps you're following in the link above is connecting you're github account with your ide. This will make it easier for you to upload your projects onto Github (remote) without having the need to sign in everytime.
---
## Repository Setup
> Now that you have set up your ide and your Github account you can now create repositories.

* Go to the directory you desire to turn into a repository
* Type `git init` in the command line
* Now you need to create a file that you can edit and make changes to
    * In the command line type `touch <filename>`
* Once you've made the file type `c9 <filename>` to open the new file
* In this file you can type anything you want
* Once you're done making edits in the file go back to the command line and type `git add .`
* Now still in the command line type `git commit -m "short/specific message"`
    * The short/specific message should be in the present tense and also describe what you change you did in the file.
* Once you have commit (saved the changes) you can now go back and do some more edits in the file.
* Now repeat:
    * Edit your file, add it and commit it


---
## Workflow & Commands
> You've just used `git init` , `git add` & `git commit` but you really dont know what they exactly do. Bellow is a list of commands you have already used and commands you haven't used that will come in handy.

REMEMBER **ALL** these commands are typed in the command line:

`git init` - This command initializes the git in a directory
* If git is initialized in a directory its now called a repository.
    * Do it in directory that you want to turn into repository 
    * DO NOT DO IT IN ROOT DIRECTORY 

        * `rm -rf .git` - If you ever initialize git in the wrong directory or in the root directory just tpye this command and it will un-initialize git.

> The follwoing two commands are used when you are done making edits in the file and you want to add them to the stage. Adding them to the stage allows you to save them later on.

`git add file.ext` - Adds changes for a *specific file* to the stage ready to commit

`git add .` - Adds changes of **ALL** files to the stage

`git status` - Ever wonder if you have added a file to the stage ready to commit. Well git status allows you to see what you have added or no.
> If you see `Modified: <file_name>` in red, it means you havent added it to the stage. While if you see the same text in green it means its been added to the stage and its ready to be commited.

`git commit -m "short/specific message"` -  Use this command when you are done adding your edits and are ready to be commited (saved).
* Your message *must be:*
    * In presesnt tense
    * Short
    * Specific
    * Describe the change you did in the file

> These commands above are probably the commands you're going to be using the most. On the other hand the following two commands are mostly optional and are used in the event you want to see previous commits.


`git diff` - If you ever want to see the differnce between  your current edit and the previous commit this will do the job.

`git log` - You may also just want to see your previous commits. Well in that case, this commit will display **ALL** previous commits you've done.
* Press *Control* and the *letter q* on the keyboard to get out of `git log`

#### Setting up Push and Pull


* You may want to begin backing up your local repositoties to the remote (Github).

`git push` - Send commits from local repo (ide) “up” to remote repo (github). Its like updating your local.

`git pull` - Sends commits from remote repo (github) down to local repo (ide). Its like updating your remote.

> But before using these commands we will have to set the place where the commits will go in the cloud. It will require some steps but after them you will be able to use both commands above.

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

* Now when you edit your README.md add it & commit it, you can now use `git push` or `git pull`

> What you just did was program your ide where to upload your repository in the cloud. If you didn't select SSH key you would have to be signing in every time you are going to push and pull. If you didn't use SSH and instead used HTTPS you will have to sign in to push or pull. Some of you may be wondering why you dont have to sign in when you use the SSH key. Well earlier when you set up your ide with yout github, you linked them together and so the computer is smart enough to recognize this and wont ask for your information again.

* Lets explain what the commands you put in the command line did.
    * `git remote add origin URL` - In simple words is setting up the connection between the local repo and remote repo.
    * `git push -u origin master` - The command creates a permenant bridge between the remote and the local. This allows to push without the extra origin master part that usally follows the command.

`git remote -v` - Ever want to remind yourself where the commits are being send to the cloud. Just type this and it will tell you where you can pull and push. This is similar to `git status`


#### How to Clone in your ide:

> Right above, you just learned how to back up your local repo. In the event of you local repo dissapears due to a virus, accidental deletion or even forgetting your own password, cloning can come in real handy. Follow the steps bellow to learn how to clone.

1. Go to [github.com](https://github.com/)
2. Go to your repository you cant access in your local repo (ide) on Github
3. Click on "Clone or Download" 
    * Make sure it says "Clone with SSH"
        * If it says "Clone with HTTPS" click "Use SSH"
4. Copy the URL
5. Go to your ide and make sure you are in the directory where you want this repo to go
6. Type `git clone` and paste the URL after it 
7. Press enter
    * If you are going to work in the repository make sure to `cd` into it.

`git clone` - Allows you to copy a remote repo into your local repo





---
## Rolling Back Changes

> Everyone makes mistakes and in coding its defintely bound to happen. The important things to keep in mind is how to undo them. Bellow are lists of commands that will help you undo them in the case of a mistake or  you just changed your mind.

`git checkout -- file` - After you edited your file you may change your mind and perfer the previous version over your current one. This is where this command come into use since it will "unedit" you current file.

`git reset HEAD file` - When you accidentally or change your mind over a file you added to the stage you can  "unadd" by using this command
    * In the event you forget this command you see it by typing `git status` after you had added your file(s) to the stage.

`git reset --soft HEAD file` - Sometimes you may want uncommit and this is where this command comes into use. 
> The commands above only undo commits, what you've added and edited one by one. If you want to save a little more time the following commands will undo multiple at the same time.

`git reset HEAD~1` - This command will undo what you added and the commit and take you directly to the editing phase.

`git reset --hard HEAD file` - Ever want to just go all the way back before commiting, adding and even having any edits done. Well this command will take you all the way back.

> Before learning the next command you need to know each commit has it own unique SHA code. This could be accessed by doing `git log`

`git reset --hard [first nine digit of SHA]`- This command erases the commit you made from your remote. In other words this is _"Unpushing"_ a file.