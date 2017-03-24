## Fork to use not yet merged features

- [Nested lists #3282](https://github.com/keystonejs/keystone/pull/3282)
- [FileField: show image thumbnails [WiP] #3397](https://github.com/keystonejs/keystone/pull/3397)


## `.git/config`

Makes merging PRs easier, e.g.: `git merge refs/pull/upstream/1234`

```ini
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
	precomposeunicode = true
[remote "origin"]
	url = https://github.com/cadus/keystone
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
[remote "upstream"]
	url = https://github.com/keystonejs/keystone.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
	fetch = +refs/pull/*/head:refs/pull/upstream/*
[branch "thumbnails"]
	remote = upstream
	merge = refs/pull/3397/head
```
