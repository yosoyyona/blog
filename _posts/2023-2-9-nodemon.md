---
layout: post
title: nodemon (how to install, window powershell scope)
---

I installed nodemon but whenever I tired to command nodemon, it didn't work.
It is not a difficult work to stop the server and restart it, but **automatic** way is better in many case. ;-)


## how to install nodemon
```bash
$ npm install nodemon --global
```

## The error message in Powershell in VScode

```bash
$ nodemon index.js

nodemon : File C:...\AppData\Roaming\npm\nodemon.ps1 cannot be loaded because running scripts is disabled on this system. For more i
nformation, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ nodemon index.js
+ ~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess 
```
So I visited the [website](https:/go.microsoft.com/fwlink/?LinkID=135170) and I realized what was the problem. So I changed the policy.

```bash
$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUserlass
```
and then
```bash
$ nodemon index.js

[nodemon] 2.0.20
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node index.js`
```
## Error solved and the server is updated automagically✨