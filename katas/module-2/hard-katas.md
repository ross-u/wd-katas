## Week 6 Hard Katas



- [Street Fighter 2 - Character Selection](https://www.codewars.com/kata/street-fighter-2-character-selection/train/javascript)



<br>



- [Playing with digits](https://www.codewars.com/kata/playing-with-digits/train/javascript)

```js
function digPow(n, p) {
  var x = String(n).split("").reduce((acc, num, i) => acc + Math.pow(num, p + i), 0)
  return (x % n ? -1 : x / n)
}
```



<br>



- [Directions Reduction](https://www.codewars.com/kata/directions-reduction/train/javascript)

```js
function dirReduc(plan) {
  var opposite = {
    'NORTH': 'SOUTH', 'EAST': 'WEST', 'SOUTH': 'NORTH', 'WEST': 'EAST'};
  return plan.reduce(function(dirs, dir){
    
      if (dirs[dirs.length - 1] === opposite[dir])
        dirs.pop();
      else
        dirs.push(dir);
      return dirs;
    }, []);
}
```
