---
layout: default
comments: true
---

# SAP Web Application Development
Traditional SAP and its ERP system use a centralized configuration and code version control system.  This type of approach has many disadvantages, especially when many developers are working on the same code base.  Modern SAP, that is a suite of distributed applications across many technology systems, uses git for code management.  SAP has also aligned with the open source movement and has sponsored and encouraged many open source tools to help you develop SAP or non-SAP web business applications.  Git has made the use of open source products workable.

The first skill that is fundamental in open source and modern distributed computing web applications (where an app can connect into many endpoints across many systems) is to have a clear understanding of git and repository stores like github.com.

The HANA XSA system and the SAP Cloud web IDE, use git.

## Git Repository Version Control
### Why Git?

Git evolved to support the LINUX open source project.  It is a decentralized code tracking system.  Developers clone and or fork the code base from a remote repository.  A copy of the entire code base is copied locally.  During development, the developer may request changes to the code base since cloning to be updated directly onto his/her local working copy.  There is no limit to the number of developers that pull the code base.  When developers wish to introduce their code changes into the central remote repo, they do so via a pull request.  A pull request will indicate if there are code conflict that needs to be resolved upon approval of the pull request.  Each developer creates a branch to do their code changes, so they have a local ability to know the code changes they are making.  Git follows the UNIX philosophy of programming where programs do only one thing and do that well.  The branches, therefore, represent the listing of proposed changes to a code repository.  Each branch undergoes automated unit and regression testing (this is a condition of acceptance of the pull request).  When a release is decided, due to the nature of git, the repo owner can selectively decide on which requests to include or not include.  Without harm to the integrity of the testing.  At all points in the process, it is possible to change the code base back to a specific release or branch point.  Or fast forward.

### Git vs SVN?

Subversion systems track code via a central code repository where users check out a version of the code, where the developer then makes his/her code changes.  The developer then checks in the code so that other developers can then make changes.  In this central coding system developers often conflict with one another, as there is only one code base.  Checking out prevents specific sections of the code base from receiving conflicting changes.  However, this is very limiting as the development team gets large and geographically separated.
A decentralized distributed code version system allows for a large community of developers to work on the same code base.  This is a major challenge with SVN systems.  This is how the LINUX kernel was developed and continues to be enhanced under.  Each issue fix, new enhancement, all get a branch, where that branch must undergo code reviews and automated testing before it can be pulled back into the remote master branch.  There can be many branches.  This is what gives git its power, as code changes are vetted, then merged into the code base.  Never do developers code in the same code repository branch. and the master branch can only be updated via approved pull requests.  These unique features of developing locally with an entire copy of the code base is was has made open source software development possible and why it is now the preferred software development method.

### SAP ABAP Transport Process Limitations 
The SAP programming language ABAP is managed using an SAP proprietary code version control and transporting system.  The way the system is designed with a high degree of integration, it requires that projects be large in scope, and testing efforts are not tied to specific enhancements but rather larger projects.  This coding method follows an error of time forward, where it must reverse out all changes to revert a prior enhancement.  SAP's method, has resulted in no open source participation and proprietary closed source code.  SAP has now adopted a git approach to web app development with HANA XS, XSA, Extended etc.

### Distributed Rather Than Centralized
This is why git is better.  Every change is tested against a complete code set.  During development, this code base can be updated from the current master code base.

How to start a git repository
~~~
git init
~~~
or

~~~
git clone https://github.com/KetchPartners/sapcommercialprojects.git
~~~

### Git is Fast Because it is Local

The local repo is a copied version of the remote repositories code base at a specific point in time.  The remote repository is often called 


~~~
origin
~~~

To apply recent remote repository updates (origin means remote and master is the remote branch that is considered the latest stable version):


~~~
git fetch origin master
~~~

### Branching and Merging

When a developer brings it locally, they often create a branch to represent the specific change the developer is going to make.  

~~~
git branch issue-12
~~~

Then the developer checks out the branch (note this is not the same thing as SVN checking out, since you are local, you are doing this for you only, so you can separate out the master branch from the changes you are about to make.)

~~~
git checkout issue-12
~~~

At any point in time you can verify which branch you are in locally:

~~~
git branch
~~~

Returns with:

~~~
master
****issue-12
~~~

The ***** points to the current branch you are working with.

There are many tools you can add to your .bash_profile to enhance your command line experience.  You can also use other bash scripting projects like .zsh. 

To install zsh shell:
~~~
git clone git://git.code.sf.net/p/zsh/code
~~~

A slicker option is to install oh-my-zsh.
[Oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh).  
You can install via wget or curl to get the build script:

~~~
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
~~~

### Other Benefits of Git

- Git is fast compared to other code version systems.
- Git is accurate as it uses rock-solid security methods and protocols.
- Git is proven a better way to code, and you gain the power of open source to your project.

### Git and Open Source
Git is open source and therefore it has replicated into many different flavors and tools to make the git process easier.  This is the key feature of open source, it enables people to take code and change it to apply to make their life easier, and also publish the change for others to make their life easier.  Git is open source and helps auto facilitate large numbers of developers modify the same code base.  Some of these changes will be pull requested back into the same git open source project.  Other changes get forked and entirely new open source products based on git.  

Examples of Notable Git Forks
[Git for Windows](https://git-for-windows.github.io/)
[Github Git Desktop](https://desktop.github.com/)

## Package Managers and Dependency Management
A Package Manager a collection of software tools that manage the installation, configuration, dependency management, updates, and uninstalling of software packages. A package manager deals with packages that contain archive file, metadata about a package, required dependencies, open source license, version, and checksum information.
Binary PackageSource code based, housed at a remote repository (ie. github.com).  Binary packages require the cloning or forking of the remote repository locally.  Build scripts are then initiated manually.  Whereas a non-source code based package manager will install and update dependencies, before the package is installed.

### Important Package Managers for Web App Development

|OS             |Package Manager |
|:--------------|:---------------|
|Ubuntu         |apt, apt-get    |
|Fedora         |yum             |
|Mac            |brew            |
|windows        |Chocolatey      |
|               |NuGet           |

### Important Application Package Managers

|Application    |Package Manager |
|:--------------|:---------------|
|Phython        |Anaconda        |
|Cloud          |Bitnami         |
|PHP            |Composer        |
|Java           |Maven, Ivy      |
|Javascript     |npm             |
|Ruby           |Rubygems        |

### Github List of Important Package Managers
[Github curated list of package managers](https://github.com/showcases/package-managers) 

### Open Source and Package Management
Open source is a key driver for the use of package managers within your web application.  Open source projects have strict copyright conditions.  Open Source is not free software, it is a package of program code, that you have complete access to the source code under a special open source license.  This license is a copyright, that allows for copying, modifying as long as certain conditions are met.  Package managers often bundle open source code that shares similar open source license requirements under one umbrella.  Without package managers, it would too complex to handle dependency and license management.  The open source license often requires changes/adaptations to code to be available publically in a forked copy of the repository.  This leads to the sharing and reuse of code programs, code snippets amongst developers.
Package Managers and Remote Repositories are what enables open source to work.  Without them, open source would be not worth it and too complex.  A typical modern web application can use hundreds of packages in a project.

## Training Exercises

Please complete the training exercises outlined [next page](https://ketchpartners.github.io/sapcommercialprojects/training-git-exercise.markdown)
