### View GIT remote details

```sh
git remote -v
```
### Add new reference with your local branch 

```sh
$ git remote add upstream GIT SSH URL

```

### Update GIT with upstream and master branch 

```sh
git fetch upstream
```

### Create new branch with upstream 

```sh 
$ git branch --track feature/name-of-the-feature upstream/develop

```
### Checkout new branch 

```sh 
$ git checkout feature/name-of-the-feature
```

### Push changes with local fork 

```sh 
$ git push origin
```
