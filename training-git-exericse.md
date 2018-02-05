---
layout: default
comments: true
---

## Install Git Command Line (Exercise 1)
To fully understand git, it is important to start with the command line.  GUI versions exist, which are great, but nothing beats the command line.  And web app developers need to write build scripts, so understanding how to use git via the command line is important. 

The easiest way to install git, it to use your package manager and your bash shell.

MAC
```
brew install git
```

Windows
```
https://git-scm.com/download/win
```

There is also the unofficial git open source projet "Git for Windows".  This gives you a bash like CLI plus a GUI version.

[Git for Windows](https://gitforwindows.org/)

There is also a desktop version available for LINUX, MAC or WINDOWS at:

[Github Desktop](desktop.github.com)

When complete exercise 1 please at bottom of this page, indictae exercise 1 complete by posting.  If you have questions or get stuck also post a comment.

## Setup Git and Create Github Account (Exercise 2)

You can set up a github account via [github.com](https://www.github.com)

When you set up your github account, send a message to me by mentioning me in post @davebeach.

Send a request to join the Ketch team for this project at
@KetchPartners/ketchuss

Click on you at top right hand icon and select SETTINGS > SSH and GPG Keys

Follow the instructions by clicking on the link in SSH and GPG sections.  This will guide you on settings up public and private keys for authentication.  If you have problems post a comment at bottom of this page.  For windows 7 users use Git For Windows Git Bash.  For windows 10, install linux distro to your system, then use command prompt to execute steps.

Now we want to set our git config, as we now have our git user name.

Replace items in [] with actual values representing you.
```
 git config --global user.name "[name]"
```

```
 git config --global user.email "[email address]"
```

```
 git config --global color.ui auto
```

For windows users and others - read [Understand Line Endings and Potential Problems](https://help.github.com/articles/dealing-with-line-endings/)

If you have successfully set up git, created a github account, sent a message to @davebeach, requested access to @KetchPartners/ketchuss, set up SSH keys on your machine, and set up GPG keys.  

## Next Training Session  

The next training session will be on-site Ramesey, NJ.  We will then take git and apply it against practical use cases with HANA XSA.

To indicate you are completed this training session, please leave comment below.  Also if you receive any error when trying please post an issue at this repo [KetchPartners/sapcommercialprojects](https://github.com/KetchPartners/sapcommercialprojects/issues)
