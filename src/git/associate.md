## associate multiple repository
### First type
```git remote add <name> <url>```
Add multiple remote repositories and named them.

```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	ignorecase = true
[remote "origin"]
	url = https://gitee.com/name/project_1.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = github
	merge = refs/heads/master
[remote "github"]`
	url = https://github.com/name/project2_2.git
	fetch = +refs/heads/*:refs/remotes/github/*

```

### Second type
``` git remote set-url --add <name> <url> ```
Specific the associated link to the particular repository.
Pay attention to the order of remote labels
```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	ignorecase = true
[remote "origin"]
	url = https://github.com/name_1/project_2.git
	url = https://gitee.com/name_2/project_1.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
```




[link]: https://git-scm.com/docs/git-remote
[link2]: https://www.jianshu.com/p/2952650fe0c2