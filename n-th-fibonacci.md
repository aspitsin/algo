# N-th Fibonacci 6 kyu

https://www.codewars.com/kata/n-th-fibonacci

MY SOLUTION

```javascript
function nthFibo(n) {
  let a = 0;
  let b = 1;
  if(n===1)return 0; // для певрого числа
  for (let i = 3; i <= n; i++) {
    let c = a + b;
    a = b;
    b = c;
  }
  return b;
}
```

INTRESTING SOLUTION 

- FIRST 

```javascript
function nthFibo(n) {
  let [prev, curr] = [0, 1];
  for (let i = 1; i < n; i++) [prev, curr] = [curr, prev + curr];
  return prev;
}
```

- SECOND 

```javascript
function nthFibo(n) {
  let a = 0, b = 1;
  
  for (let i = 3; i <= n; i++) {
    let c = a + b;
    a = b;
    b = c;
  }
  return n == 1? a: b;
}
```
