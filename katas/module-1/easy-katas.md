# Week 3 Easy Katas

- [List Filtering](https://www.codewars.com/kata/list-filtering/javascript)

```js
function filter_list(l) {
  return l.filter(item => typeof item === 'number')
}
```

<br>

- [Sum of all the multiples of 3 or 5](https://www.codewars.com/kata/sum-of-all-the-multiples-of-3-or-5/javascript)

```js
function findSum(n) {
  let sum = 0;
  for (let i = 0; i <= n; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
}
```

<br>

- [Vowel Count](https://www.codewars.com/kata/vowel-count)

```js
function getCount(str) {
  return str.split('').filter(letter => 'aeiou'.includes(letter)).length
}
```

<br>

- [Flatten](https://www.codewars.com/kata/flatten-1/javascript)

```js
var flatten = function(array){
  return [].concat.apply([],array)
}
```

<br>

- [Growth of a Population](https://www.codewars.com/kata/growth-of-a-population/train/javascript)

```js
function nbYear(p0, percent, aug, p) {
    var year = 0;
    while (p0 < p) {
      p0 += (p0 * (percent/100)) + aug;
      year++;
    }
    return year;
}
```

<br>

- [Credit Card Mask](https://www.codewars.com/kata/credit-card-mask/javascript)

```js
function maskify(cc) {
  var ccArr = cc.split('');
  return ccArr.map((num, i) => {
    if (i >= ccArr.length - 4) {
      return num;
    } else {
      return '#';
    }
  }).join('');
};
```
