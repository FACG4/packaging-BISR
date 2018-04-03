# packaging-BISR

###### This is not a new topic to learn ,it will clear the confusion if found by (Balsam , Ishak , Salam and Razan ) .


**_ 1 . Dependencies : _**

Programs often use some of the same files as each other. Rather than putting these files into each package, a separate package can be installed to provide them for all of the programs that need them. So, to install a program which needs one of these files, the package containing those files must also be installed. When a package depends on another in this way, it is known as a package dependency. By specifying dependencies, packages can be made smaller and simpler, and duplicates of files and programs are mostly removed.


**_ scratch _** : creating the code from zero

**_ Benefits of dependencies _** ?

 * Higher speed/ performance .


* Better interoperability with other software .

* Take better advantage of the newer operating systems or server side software or new services .

* Smaller footprint in terms of memory and other resources .

* Take advantage of new technology available for creating the software .

* Take advantage of new intellectual property thus created.

**_ What have traditionally been some of the issues with managing dependencies? _**

Problem #1: Lack of End-to-End Visibility
Making dependencies visible (and then managing them across projects) is probably the most important problem(s) we’ve encountered.

Problem #2: Bad Solutions for Lack of Visibility
Each manager may use a different solution, which only compounds the difficulty of managing the dependency efficiently.

Problem #3: Teams’ Own Unique Perspectives .


**_ 2 . NPM : _**

-The NPM program is installed on your computer when you install Node.js .

-A package in Node.js contains all the files you need for a module.

-To Initialise package using npm, we use the command:
```
npm init
```

-To install package, write :
```
npm install your-package-name
```
then to use it, write :
```
var uc = require('your-package-name');
```

**_ 3 . Installation of NPM : _**

* Locally :

```
npm install module_name
```

* Globally :

```
npm install -g module_name
```

* Differences between dependency and  development dependency :

the first is to the prodution (run time) , and the last is for developers .

**_ 4 . NO PUSH : _**


**_ Where does NPM install packages? _**

Installing Packages in Local Mode
When you install packages locally, you normally do so using a package.json file. Let’s go ahead and create one.
```
$ npm init
```
package name: (project)
version: (1.0.0)
description: Demo of package.json
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
Press Enter to accept the defaults, then type yes to confirm. This will create a package.json file at the root of the project.
{
"name": "project",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
"test": "echo \"Error: no test specified\" && exit 1"
},
"author": "",
"license": "ISC"
}

**_ Tip: _** If you want a quicker way to generate a package.json file use
```
npm init --y
```
**_ Why is it important to make sure that installed packages aren't included in your repositories? _**

The repositories should be kept under 1GB each. This limit is easy to stay within if large files are kept out of the repository. If your repository exceeds 1GB, you might receive a polite email from GitHub Support requesting that you reduce the size of the repository to bring it back down.
so we shouldn't push the packages file more than once.

**_ How do you prevent Git from including these files in your repository? _**

simply by adding the “gitignore” file when you pushing your code to the git.
