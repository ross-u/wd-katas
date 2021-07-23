## MODULE 3 Hard Katas

- [Sum of Pairs](https://www.codewars.com/kata/sum-of-pairs/javascript)

```js
var sum_pairs=function(ints, s){
  var seen = {}
  for (var i = 0; i < ints.length; ++i) {
    if (seen[s - ints[i]]) return [s - ints[i], ints[i]];
    seen[ints[i]] = true
  }
}
```



<br>



- [All that is open must be closed...](https://www.codewars.com/kata/all-that-is-open-must-be-closed-dot-dot-dot/javascript)



<br>



- [Scramblies](https://www.codewars.com/kata/scramblies/)

  

<br>



- [Bit Counting](https://www.codewars.com/kata/526571aae218b8ee490006f4)

```js
var countBits = function(n) {
  let bin = n.toString(2).split('').sort();
  let num1 = 0;
  for(let i=0; i<bin.length; i++){
    if(bin[i] === '1'){
      num1++
    }
  }
  return num1
};
```



<br>



- [Pete, the baker](https://www.codewars.com/kata/pete-the-baker/)



<br>



## Week 9 Hard Katas
- [Playing with digits](https://www.codewars.com/kata/playing-with-digits)

  

<br>



- [Take a Ten Minute Walk](https://www.codewars.com/kata/take-a-ten-minute-walk/javascript)

```js
function isValidWalk(walk) {
  var dx = 0
  var dy = 0
  var dt = walk.length
  
  for (var i = 0; i < walk.length; i++) {
    switch (walk[i]) {
      case 'n': dy--; break
      case 's': dy++; break
      case 'w': dx--; break
      case 'e': dx++; break
    }
  }
  
  return dt === 10 && dx === 0 && dy === 0
}
```
