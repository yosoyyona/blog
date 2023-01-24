---
layout: post
title: git push error(fetch first, non-fast-forward)
---



$ git push

# ! [rejected]      main -> main (fetch first)
error: failed to push some refs to ...
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

<googling>
https://stackoverflow.com/questions/28429819/rejected-master-master-fetch-first

$ git fetch
remote: Enumerating objects: 11, done. 
(...)

$ git push

# ! [rejected]      main -> main (non-fast-forward)
error: failed to push some refs to ...
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

<googling>
https://stackoverflow.com/questions/20467179/git-push-rejected-non-fast-forward

$ git commit -m"merging"
$ git pull
$ git push

✨Error solved!