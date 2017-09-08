# Codewars---Gap-in-Primes

```
function gap(g, m, n) {
    // your code
  var allNumbers = [];
  var primeNumbers = [];
  
  for (var i = m; i <= n; i++) {
    allNumbers.push(i);
  }
  
  allNumbers.forEach(function(ele) {
    if (ele % 2 !== 0) {
      for (var i = 3; i < Math.sqrt(ele); i = i + 2) {
        if (ele % i == 0) {
          break;
        }
      }
    }
    
    if (i > Math.floor(Math.sqrt(ele))) {
      primeNumbers.push(ele);
    }
    
    /*var count = 2;
    for (var j = 2; j < ele; j++) {
      if (ele % j !== 0) {
      count++;
      }
    }
    if (count > ele - 1) {
      primeNumbers.push(ele);
    }*/
  });
  
  for (var k = 0; k < primeNumbers.length - 1; k++) {
    if (primeNumbers[k + 1] - primeNumbers[k] === g) {
    return [primeNumbers[k], primeNumbers[k + 1]];
    }
  }
  
  return null;
}
```
