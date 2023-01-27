---
layout: post
title: git push error(fetch first, non-fast-forward)
---

I got some error when I pushed some change of code.

First error message was "fetch first"
To solve it, "git fetch"

```bash
$ git push

# ! [rejected]      main -> main (fetch first)

error: failed to push some refs to ...
Updates were rejected because the remote contains work that you do not have locally. This is usually caused by another repository pushing to the same ref. You may want to first integrate the remote changes (e.g., 'git pull ...') before pushing again. See the 'Note about fast-forwards' in 'git push --help' for details.
```


## [Here's the answer!](https://stackoverflow.com/questions/28429819/rejected-master-master-fetch-first)


```bash
$ git fetch
remote: Enumerating objects: 11, done. 
(...)
```

---

I tried to push it but I got a second error message of "non-fast-forward"
To solve it, "git commit" and "git pull"
And then "git push"!

```bash
$ git push

# ! [rejected]      main -> main (non-fast-forward)

error: failed to push some refs to ...
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```


## [Here's the next answer!](https://stackoverflow.com/questions/20467179/git-push-rejected-non-fast-forward)

```bash
$ git commit -m"to merge"
$ git pull
$ git push
```


## ✨Error solved!