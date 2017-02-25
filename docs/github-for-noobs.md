# GitHub For N00bs
This is an introduction to GitHub and Git on the example of contributing to AngelArenaAllstars.

We start at blank. No repo - nothing.

## But first some terminology
GitHub and Git are not the same!
#### Git
>Git - fast, scalable, distributed revision control system

[Git on GitHub](https://github.com/git/git)
#### GitHub
>GitHub is a web-based Git or version control repository and Internet hosting service.

[Wikipedia](https://en.wikipedia.org/wiki/GitHub)
#### AngelArenaAllstars/aaa
The Repository `aaa` of the Account `AngelArenaAllstars`

### Now follow the [Installation Process](/docs/install.md) until [`Get The Addon`](docs/install.md#get-the-addon)

Instead of just [cloning](https://www.git-scm.com/docs/git-clone) (copying a repository) we'll create a fork and work from there.
I assume you already have a GitHub.com Account; if not create one [here](https://github.com/join).

## Setting things up
### Forking
1. Goto [AngelArenaAllstars/aaa][AAA/aaa].
![Repository Overview](/docs/github-for-noobs/Repository-Overview.png)
2. Click ![Fork](/docs/github-for-noobs/Fork.png)
3. Choose where to fork [AngelArenaAllstars/aaa][AAA/aaa] (usually your own Account).
![Fork Dialog](/docs/github-for-noobs/Fork-Dialog.png)
4. Done. If you go to `https://github.com/<YOURUSERNAME>/aaa` you'll see your own fork of [AngelArenaAllstars/aaa][AAA/aaa].

### Cloning your Fork of [AngelArenaAllstars/aaa][AAA/aaa].
You can do basic things with the GitHub Client but I don't know how. They ship a nice Shell Integration for PowerShell wich will be really useful later.

Open the GitHub Client you installed earlier in [install.md](/docs/install.md).
![GitHub Client Overview](/docs/github-for-noobs/GitHub-Client.png)

First go to settings.

![GitHub Client Settings Button](/docs/github-for-noobs/GitHub-Client-Settings.png)

Change the settings how you like it (e.g. Change to Dark mode).
However I recommend changing the default shell to PowerShell.

![GitHub Client Settings Shell](/docs/github-for-noobs/GitHub-Client-Shell.png)

**CLICK SAVE!**
![GitHub Client Settings Save](/docs/github-for-noobs/GitHub-Client-Save.png)

Click on ![GitHub Client Add](/docs/github-for-noobs/GitHub-Client-Add.png) in the upper left corner.

Select Clone ![GitHub Client Add-Create-Clone](/docs/github-for-noobs/GitHub-Client-Tab.png)

Select your Account and the forked `aaa` repository
![GitHub Client Clone](/docs/github-for-noobs/GitHub-Client-Clone.png)

Click ![GitHub Client Clone Button](/docs/github-for-noobs/GitHub-Client-Clone-Button.png)

Now we should have a local copy of your fork of [AngelArenaAllstars/aaa][AAA/aaa]

### Open Git Shell
You can do this via the shortcut on your Desktop or in your Startmenu
Or via this command
`%USERPROFILE%\AppData\Local\GitHub\GitHub.appref-ms --open-shell`
* (Recommended) Or you Right-Click in the GitHub Client on your repository entry and select `Open in Git Shell`

![Open Git Shell](/docs/github-for-noobs/GitHub-Client-Contextmenu.png)

Now we should have something rougly like this
![GitShell](/docs/github-for-noobs/GitShell-Start.png)
 
### Before we continue here finish the [Installation Process](/docs/install.md) after [`Get The Addon`](docs/install.md#get-the-addon)

## Keeping your copy of [AngelArenaAllstars][AAA/aaa] uptodate
To be able to work on our own stuff but still have all the newest changes and to have a nice and organized repository, git features branches.
Read [Git Branching - Branches in a Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

### To keep the `master` Branch uptodate
Let first look at the different remotes we have
```
> git remote -v
origin  https://github.com/<YOURUSERNAME>/aaa (fetch)
origin  https://github.com/<YOURUSERNAME>/aaa (push)
```
*origin* is where your local repository comes from.

Now we'll add another remote to make updating easier
```
> git remote add AngelArenaAllstars https://github.com/AngelArenaAllstars/aaa
```
You do not have to call this remote AngelArenaAllstars, you can call it whatever you want.

Get the newest changes from [AngelArenaAllstars/aaa][AAA/aaa]
```
> git pull AngelArenaAllstars master
From https://github.com/AngelArenaAllstars/aaa
 * branch            master     -> FETCH_HEAD
Already up-to-date.
```

Now we have the newest changes on the local master branch.
We also want them on GitHub
```
> git push
Everything up-to-date
```

### Start working
To do this we want our own branch for this feature hotfix path whatever.
Always make sure you're in the master Branch
```
> git checkout master
Your branch is up-to-date with 'origin/master'.
Switched to branch 'master'
```

Create and switch to your new branch
```
> git checkout -b awesome-branch
Switched to a new branch 'awesome-branch'
```

Now you can do your changes!

To commit your changes you can either use GitHub Desktop or do
```
> git commit <YOUR CHANGED FILES> -m "WHAT YOU CHANGED" -m "A OPTIONAL EXTENDED DESCRIPTION"
[github-for-noobs 3be214d] more changes
 1 file changed, 19 insertions(+)
```

Now push your changes to GitHub
```
> git push
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 600 bytes | 0 bytes/s, done.
Total 4 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/Chronophylos/aaa
   1554bf2..3be214d  github-for-noobs -> github-for-noobs
```

### Creating a PR
To create a PR goto [AngelArenaAllstars/aaa][AAA/aaa] on GitHub

Click ![New Pull Request](/docs/github-for-noobs/New-PR.png)

Click `compare across forks`

![compare across Forks](/docs/github-for-noobs/Compare-Across-Forks.png)

Click `head fork` and choose your Repository

![select Head Fork](/docs/github-for-noobs/Head-Fork.png)

Click `compare` and select your Branch

![select Head Branch](/docs/github-for-noobs/Head-Branch.png)

Now fill in the form ![PR Description](/docs/github-for-noobs/PR-Description.png)

Click ![Create pull request](/docs/github-for-noobs/Create-PR.png) and you're done!



___
Bored? [Read the entire Pro Git Book](https://git-scm.com/book/en/v2)!

If you have Questions/Problems at least try and google first. A lot of them are already answered on [Stack Overflow](https://stackoverflow.com/questions/tagged/git).

But if that didn't help or you are not sure, feel free to ask me on Discord@Chronophylos#5199 or via Twitter [@Chronophylos](https://twitter.com/Chronophylos)(a response is unlikely)

[AAA/aaa]: https://github.com/AngelArenaAllstars/aaa "AngelArenaAllstars' aaa Repository"
