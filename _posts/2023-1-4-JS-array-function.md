---
layout: post
title: JS | Array Function - reduce method (stuck)
---

Yesterday I learned map, reduce & filter methods of array function in the class.
Recapping the contents I stuck in a problem.


📝 Exercise

const menu = [
  { name: 'Carrots', calories: 150 },
  { name: 'Steak', calories: 350 },
  { name: 'Broccoli', calories: 120 },
  { name: 'Chicken', calories: 250 },
  { name: 'Pizza', calories: 520 }
];
 
// your code:
 
console.log(averageCalories); // 278


🐲 My code

const averageCalories = menu.reduce(function(sum, food) {
    
    return Math.round((sum + food.calories) / menu.length)
    
}, 0)


But my result is 116. 
What did I miss? 🤔 