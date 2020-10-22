#### Github:

###### create a local git configuration for our account



```
git config --global user.name "sushmasiram"

git config --global user.email "sushma.motamarri@gmail.com"
```



###### Files navigation in gitbash

ls: list the items of current location

pwd: present working directory

mkdir: make a new directory

cd: change a directory
cd desktop/coding/

vi <file_name> -- to open a file in editor
vi angrybirdsv2.5

i -- to edit the file.. we should use this after opening the file using vi <file_name>

after making the changes in the file.. click 'esc' button to come out of the insert mode

:w --- to save changes in the file, after coming out of the insert mode

:q-- to exit from vi . 

:wq -- to save changes and exit from vi editor.



###### clone a repo to local

git clone https://github.com/whitehatjr/bouncyBall

git status - To see any new updates that are to be commited

git log - To see history of the repo

git add <filename> to add a single file to the git repo

git add sketch.js

git add .   Adds all the files that are edited

git commit     commits the changes

git commit -m "any message" -- this is to commit all the files to the local repository 

###### 


-- create an empty repository in git hub, and get the https url from the page.

-- Now add our local repository to the empty git hub repository.

 git remote add <empty repository name> <empty repository url>

-- Now push all the files from our local sytem to the empty repository .

git push -u <empty repository name> 
