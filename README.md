# wildcodeschoolKata

Please take 5-10 minutes and try one of the exercise which you want to master it.

### LVL 1  -  Back up project
back-up your projects by creating a copy of your directory with all the files and copy to *back-up* dir; reset enviroment


```shell
#backup project
mkdir project 
mkdir backup
cd project
touch file_1.txt
echo "#test 1" > file_1.txt
cat file_1.txt
echo "#test 2" > file_2.txt
cat file_2.txt
cd ..
cp -R project backup
cd backup
ls
cd project
ls
cd ../../

#clean up
rm -rf backup
rm -rf project
```
### LVL 2  -  Git basic (localhost) 
Create a project dir and create a git project. Create 2 branches : master , develop. Create a new branch respecting GIT FLOW aproach . The new branch is copy of develop and the name is *feature/TICKER-NO-Component*. Create a new file and add some modifications to it. Commit all the changes to the branch *feature/TICKER-NO-Component* . Merge the branch with *develop* branch (solve the conflicts in case) . Delete the branch *feature/TICKER-NO-Component*; reset enviroment

```shell
#create project
mkdir git_project
cd git_project
git init
git checkout develop
git checkout feature/ticket-number-my-Component
echo "my first code" > file_1.txt
git add file_1.txt
git status
git commit -m "add Component"
git checkout develop
git merge checkout feature/ticket-number-my-Component
git branch
git branch -D feature/ticket-number-my-Component
git branch

#clean project
cd ..
rm -rf git_project

```

### LVL 3  -  Learn Shortcuts Commands from IDE
Open Favorite IDE ( WebStorm, Visual Studio Code, Atom, SublimeText3) and practice commands from the keybords (define shortcuts for it):
1. open terminal in IDE
1. hide panel with root project (tree structure)
1. Open a javascript file (not empty)
1. duplicate line
1. delete entire line
1. save file
1. search and replace

VISUAL STUDIO CODE:
import shorcuts from Intellij Idea
https://marketplace.visualstudio.com/items?itemName=k--kato.intellij-idea-keybindings

### LVL 4  -  Install dependencies using NPM commands
use terminal and install 5 packages; 
requirement: Nodejs installed; [install Nodejs] (https://nodejs.org/en/download/)
```shell
#create project
mkdir npm_kata
cd npm_kata

# working with npm
npm init
npm install  yarn
npm install  npx
npm install  np
npm install  npm-name-cli

# debugging
npm install  ndb
npm install  node-inspector

# general utilities
npm install  tldr
npm install  now
npm install  spoof
npm install  fkill-cli
npm install  castnow
npm install  github-is-starred-cli
npm install  vtop

# react
npm install  create-react-app
npm install  create-react-library
npm install  react-native-cli

# linting
npm install  eslint
npm install  babel-eslint
npm install  eslint-config-standard
npm install  eslint-config-standard-react
npm install  eslint-config-standard-jsx
npm install  eslint-plugin-react
npm install  eslint-config-prettier
npm install  eslint-plugin-prettier
npm install  prettier
npm install  standard
npm install  typescript

#clean project
cd ..
rm -rf npm_kata
```


### LVL 5  -  Config NPM Scripts in package.json
Create a file package.json with a basic scheleton; define a command script for testing JS files; Run the scripts in the console.
links: ["how to create npm scripts"](https://medium.freecodecamp.org/introduction-to-npm-scripts-1dbb2ae01633)

```shell
#create project
mkdir npm_project
cd npm_project

npm init
```
![alt text](https://raw.githubusercontent.com/crisanlucid/wildcodeschoolKata/master/assets/images/npm_config_package.png)

```shell
npm i http-server
```

define script alias "server" in package.json to run a command for the http-server module with port 3000

![alt text](https://raw.githubusercontent.com/crisanlucid/wildcodeschoolKata/master/assets/images/img_package.json.png)


```shell
#clean project
cd ..
rm -rf npm_project
```
### LVL 6 - Git flow (localhost + remote) 
https://drive.google.com/file/d/1qqjCHO7Ndqp1cyp2M8nfRhdyK5PW5rtq/view?usp=sharing

### LVL 7 - Git Undo last commit (advanced + localhost)
resource: [here] (https://www.jquery-az.com/undo-last-commit-in-git/)

By using the **-soft** flag, you may keep the changes in the last commit while moving the HEAD pointer back to the last commit
By usung  the **–hard** flag with reset command. So, you have to be careful as reverting back to last commits. You may lose your important files if undone carelessly.


```shell
#create project
mkdir git_project
git init

touch alpha.txt
git add . & git commit -m "Local commit #1"
touch beta.txt
git add . & git commit -m "Local commit #2"
touch lucian.js
git add . & git commit -m "Local commit #3"
touch radu.js
git add . & git commit -m "Local commit #4"
touch gabriel.js
git add . & git commit -m "Local commit #5"

#shows the history of HEAD as the git commit commands 
git reflog

#the file will be put in stage
git reset --soft HEAD~1
git commit -m "Local commit #5"

#shows the history of HEAD as the git commit commands 
git reflog

#force to be reset to previous commit
git reset --hard HEAD~1

#clean project
cd ..
rm -rf git_project
```
