# Week 6 Easy Katas



- [Jaden Casing Strings](https://www.codewars.com/kata/jaden-casing-strings/train/javascript)

```js
String.prototype.toJadenCase = function () {
return this.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ')
};

```



<br>



- [Find the odd int](https://www.codewars.com/kata/find-the-odd-int/train/javascript)

```js
function findOdd(A) {
  let result=[];
  A.forEach(number => {A.filter(v => v === number).length % 2 !== 0 && result.push(number)})
  return result[0]
}
```



<br>



- [Drone Fly By](https://www.codewars.com/kata/drone-fly-by/train/javascript)

```js
function flyBy(lamps, drone) {
  const lampsArr = lamps.split('');
  drone.split('').map((el, i) => {
    lampsArr[i] = lampsArr[i] && 'o';
  })
  return lampsArr.join('');
}
```



<br>



- [Square Every Digit](https://www.codewars.com/kata/square-every-digit/train/javascript)

```js
function squareDigits(num){
  return Number([...num+ ''].map(number=>number**2).join(''))
}
```

<br>



- [Inverting a Hash](https://www.codewars.com/kata/inverting-a-hash/train/javascript)

```js
function invertHash(hash) {
  const res = {};
  for(let key in hash) {
    res[hash[key]] = key;
  }
  return res;
}
```
