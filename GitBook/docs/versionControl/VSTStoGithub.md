# Forking from VSTS to Github

* ### There is no direct method for forking a repository from VSTS to Github

1.Clone VSTS repo to your local computer

2.Create new repository in Github and initialize with a README.md

3.Add Github repository as another remote to your local repository

``` git remote add [name] [repo url] ``` 

4.Merge local repository with the github repository you created

``` git pull [origin] [branch] --allow-unrelated-histories ```

* ```--allow-unrelated-histories``` allows you to pull from repositories with different files and commits

5.Resolve any merge conflicts and complete merge

6.Push your repository to github

* If you would like to push local work to both VSTS and Github remote repository, you can use this command:

``` 
git remote set-url --add --push origin [repo URL]
git remote set-url --add --push origin [another repo URL] 

```