---
layout: post
title: JS | Array Function - reduce method (solved)
---

Yesterday I learned map, reduce & filter methods of array function in the class.
Recapping the contents I stuck in a problem.


# 💪 Exercise
```javascript
  const menu = [
  { name: 'Carrots', calories: 150 },
  { name: 'Steak', calories: 350 },
  { name: 'Broccoli', calories: 120 },
  { name: 'Chicken', calories: 250 },
  { name: 'Pizza', calories: 520 }
];
 
// your code:
 
console.log(averageCalories); // 278
  ```


# 🐲 My code
```javascript
  const averageCalories = menu.reduce(function(sum, food) 
{
    return Math.round((sum + food.calories) / menu.length)
}, 0)
  ```

📝 But my result is 116. What did I miss? 🤔 


# ✨ Solved!
```javascript
const totalCalories = menu.reduce(function(sum, food) 
{
    return Math.round(sum + food.calories)
}, 0)

const averageCalories = totalCalories / menu.length
  ```



📝 Below there were similar exercise&solution and I looked up.
I wanted to write less code, but I had to separate in 2 processes. 
