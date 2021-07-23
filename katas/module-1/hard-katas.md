## Week 3 Hard Katas

- [Number of anagrams in an array of words](https://www.codewars.com/kata/587e18b97a25e865530000d8)

##### Solution 1
```js
function anagramCounter (wordsArray) {
  var counter = 0;
  var wordSorted = wordsArray.map((word)=>{return[...word].sort().join("");}).forEach((word, i, wordSorted)=>{
    for (var j = i; j < wordSorted.length; j++) {
      if(wordSorted[i] === wordSorted[j+1]) counter++
    };
  })
  return counter;
}
```

##### Solution 2
```js
function anagramCounter(wordsArray) {
  const sortedWords = wordsArray.map( word => word.split('').sort().join(''));
  let numberOfAnagrams = 0;

  sortedWords.forEach( (word, index) => {
    for(let i = index+1; i < sortedWords.length; i++) {
      if (word === sortedWords[i]) {
        numberOfAnagrams++;
      }
    }
  });
  
  return numberOfAnagrams;
}
```

<br>

- [TGI Friday!!](https://www.codewars.com/kata/5a0d6d8c6975982b5b000383)

```js
function lastDayIsFriday(initialYear, endYear) {
  var finalYear = endYear || initialYear
  var fridayCounter = 0;
  
  for (var year = initialYear; year <= finalYear; year++){
      for (var month = 1; month <= 12; month++){
          var date = new Date (year, month, 0);
          if(date.getDay() === 5) {
          fridayCounter++;
      };
    }
  }
return fridayCounter
}  
```
<br>

- [Clocky Mc Clock-Face](https://www.codewars.com/kata/clocky-mc-clock-face/javascript)

```js
var whatTimeIsIt = function(angle) {
  let hour = Math.floor(angle / 30);
  let min = Math.floor((angle % 30) * 2);
  if (hour === 0) {
    hour = '12';
  }
  if (hour < 10) {
    hour = '0' + hour;
  }
  if (min < 10) {
    min = '0' + min;
  }
  return `${hour}:${min}`;
};
```

- [Sort a 2D array](https://www.codewars.com/kata/587f46c9406f2dc381000009)

```js
function namesSorter (departmentsArray) {
  return [].concat.apply([],departmentsArray).sort((a,b) => a.length - b.length || a.localeCompare(b))
}
```

<br>

- [Find the missing letter](https://www.codewars.com/kata/find-the-missing-letter/javascript)

```js
function findMissingLetter(array)
{
  let found;
  array.reduce((sum, el) => {
    if (el.charCodeAt(0) > sum.charCodeAt(0) + 1) {
      found = el.charCodeAt(0)-1;
     return el;
    } else {
      return el;
    }
  });
  return String.fromCharCode(found);
}
```

<br>

- [Persistent Bugger](https://www.codewars.com/kata/persistent-bugger/javascript)

```js
function persistence(num) {
  num = num.toString().split("");
  var result = 1;
  var counter = 0
  
  if(num.toString().split("").length == 1) {
    return counter;
  } else {
    num.forEach(numStr=>{
      result = parseInt(numStr)*result;
    })
    counter++;
  }
  
  if(result.toString().split("").length > 1) {
    counter += persistence(result);
  }
  return counter;
}
```
