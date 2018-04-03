---
title: rainbow-color-by-math-random
layout: post
---

## HTML part 

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>

  <button id="change">Change</button>
  
  <script src="script.js"></script>
</body>
</html>
~~~

## Js part 

~~~js
var button = document.getElementById('change');
var rainbow = ['blue', 'violet', 'red', 'orange', 'yellow', 'green', 'rebecapurple'];

function change() {
  var random_number = Math.floor(7*Math.random());
  console.log('random_number', random_number);
  document.body.style.backgroundColor = rainbow[random_number];
}

button.addEventListener('click', change);
~~~

