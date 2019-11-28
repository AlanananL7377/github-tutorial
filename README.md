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

`git init` - This command initializes the git in a directory  
* If git is initialized in a directory its now called a repository.



---
## Rolling Back Changes