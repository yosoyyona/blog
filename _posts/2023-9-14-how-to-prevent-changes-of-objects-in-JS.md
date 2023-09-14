---
layout: post
title: How to prevent changes of objects in JS
---

I started to read tech news and today I pick up this news.
-


### [Mutability of Objects in JavaScript](https://javascript.plainenglish.io/mutability-of-objects-in-javascript-36ff13f909e3)



Objects in JS are mutable, at any time their properties can be adde, removed or modified.

**If I want to restrict how an object can be modified or prevent further changes?**

There are 3 methods to do it.
- Object.freeze()
- Object.seal()
- Object.preventExtensions()



#### Object.freeze()
- to make an object immutable, only on the first level of keys in an object
- the nested objects or array can be changed 

#### Object.seal()
- to allow the values of existing properties to be updated (not be added nor deleted); **the structure is fixed**
- the nested objects or array can be changed 

#### Object.preventExtensions()
- to allow the values of existing properties to be updated and the properties to be deleted; **the addition of new properties is prevented**
- the nested objects or array can be changed 


### Resume
||freeze|seal|preventExtensions|
|---|:---:|:---:|:---:|
|Can the properties be added?|X|X|X|
|Can the properties be deleted?|X|X|O|
|Can values be updated?|X|O|O|
|Can the nested obj/arr be changed?|O|O|O|
