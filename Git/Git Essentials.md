&nbsp;

[Git Essentials](https://www.youtube.com/watch?v=u1Zvkqjx0Ik)  
[Git Guides](https://github.com/git-guides/git-init)

&nbsp;

```
git init myrepo
```  

This command will create a a directory for your respository it will also contain a `.git`.
This contains all the settings and configurations for your repo.  

&nbsp;

```
git status
```  

This command will give you the status of the repository you have to be in the repository for it to work.

&nbsp;

```
git add filename.txt
```  

This command will add a file to version control and will show it as tracked will show as green instead of red.

&nbsp;

```
git config --global user.name "Jay LaCroix"
```  

This sets a configuration parameter for git itself it is a user wide change and will apply for all repositories you commit to.

&nbsp;


```
git config --global user.email "jay@example.com"
```  

This sets the email of the user that is working with the repositories on the system.


&nbsp;

```
git commit -m "Initial commit of filename.txt"
```  

This will add a description of the commit you are doing. Not adding the -m will open the file in a text editor.

&nbsp;

```
git diff filename.txt
```   

This command will track the changes between commits.

&nbsp;


```
git log --oneline
```  

This command will list the commits in the repository and condenses them to one line each with a hash.

&nbsp;

```
git revert 2b1487c
```  

This will revert to a previous commit using the hash of the most recent change which will open a text editor and will show the full hash that is being reverted.

&nbsp;


```
git clone githuburl.com
```  

This will download a repository from git hub with the url of the repository.

&nbsp;


```
git remote add origin "url to the repository on your github"
```  

This will change the origin of the repository which is set to the url of the repository on github that was created.

&nbsp;




### Removing files from a Repository  

To remove a file from a repository:  

```
git rm filename.txt
```  

Removing an entire directory and its contents use the `-r` option:  

```
git rm -r git rm -r  Tools/
```  

<br>

To finalize the deletion you need to make a commit:  

```
git commit -m "removed tools folder temporarily"
```    

Then finally use `git push` to remove it there as well. 

<br>  

To keep the file in the working directory but stop tracking it use:  

```
git rm --cached <file>
```  

This command will untrack the file while leaving it intact on the local filesystem.









