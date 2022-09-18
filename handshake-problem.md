# Handshake problem 6 kyu

https://www.codewars.com/kata/handshake-problem

MY SOLUTION 

```javascript
function getParticipants(h){
  if(!h) return 0;
  for(var i=0,k=1;i<h; k++);
  i = i + k;
  return k;
}
```
