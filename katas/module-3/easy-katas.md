# Week 8 Easy Katas

- [Growth of a population](https://www.codewars.com/kata/growth-of-a-population)

```js
function nbYear(p0, percent, aug, p) {
    // your code
    if (p0 >= p) {
      return 0;
    }
    
    return 1 + nbYear(p0 + p0 * percent / 100 + aug, percent, aug, p);
}
```



<br>



- [Inverting a Hash](https://www.codewars.com/kata/inverting-a-hash/javascript)
```js
function invertHash(hash) {
  inverted = {};
  
  for (const [key, value] of Object.entries(hash)) {
    inverted[value] = key;
  }
  return inverted;
}
```



<br>



- [Highest and Lowest](https://www.codewars.com/kata/highest-and-lowest/javascript)

```js
function highAndLow(numbers){
  let newNumbers = numbers.split(' ')
 return `${Math.max(...newNumbers)} ${Math.min(...newNumbers)}`
}
```


<br>



# Week 9 Easy Katas



- [Complementary DNA](https://www.codewars.com/kata/complementary-dna/javascript)

```js
function DNAStrand(dna) {
  complement = '';
   dna.split('').forEach((letter)=>{
    switch (letter) {
      case 'A':
        complement += 'T';
        break;
      case 'T':
        complement += 'A';
        break;
      case 'C':
        complement += 'G';
        break;
      case 'G':
        complement += 'C';
        break;
    }
   })


  return complement;
}
```



<br>



- [Descending Order](https://www.codewars.com/kata/descending-order/train/javascript)

```js
function descendingOrder(n){
  return [...n+''].sort().reverse().join('')*1
}
```



<br>



- [Principal Diagonal | VS | Secondary Diagonal](https://www.codewars.com/kata/5a8c1b06fd5777d4c00000dd)

```js
function diagonal(matrix){
  let principalDiag = 0;
  let secondDiag =0;

  for(let i=0; i<matrix.length; i++){
    principalDiag += matrix[i][i];
    secondDiag += matrix[i][matrix.length -1 - i];
  }
  if(principalDiag > secondDiag){
    return "Principal Diagonal win!";
  } else if (secondDiag > principalDiag){
    return "Secondary Diagonal win!";
  } else {
    return "Draw!";
  }
}
```



<br>



- [Printer Errors](https://www.codewars.com/users/tawebbcn/completed_solutions)

```js
function printerError(s) {
  var arrayOfLetters = s.split('');
  
  var counter = 0;
  
  arrayOfLetters.forEach(function(letter) {
    if (letter > 'm') {
      counter++
    }
  });
  
  return counter + '/' + arrayOfLetters.length;
}
```
