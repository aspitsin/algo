# Human readable duration format 4 kyu

https://www.codewars.com/kata/human-readable-duration-format

MY SOLUTION 

```javascript
function formatDuration(n) {
  let arr = [];
  if(!n) return 'now';
  if(!((n / 31536000) < 0)) {
    let years = Math.floor(n / 31536000);
    if(years > 0){
      n = n - (years * 31536000)
      let res = years === 1 ? `${years} year` : `${years} years`;
      arr.push(res)
    }
  }
  if(!((n / 86400) < 0)){
    let days = Math.floor(n / 86400);
    if(days > 0){
      n = n - (days *  86400);
      let res = days === 1 ? `${days} day` : `${days} days`;
      arr.push(res);
    }
  }
  if(!((n / 3600) < 0)){
    let hours = Math.floor(n / 3600);
    if (hours > 0 ){
      n = n - (hours *  3600);
      let res = hours === 1 ? `${hours} hour` : `${hours} hours`;
      arr.push(res);
    }
  }
  
  if(!((n / 60) < 0)){
    let minutes = Math.floor(n / 60);
    if (minutes) {
      n = n - (minutes * 60);
      let res = minutes === 1 ? `${minutes} minute` : `${minutes} minutes`;
      arr.push(res);
    }
  }
  if(n) {
    let seconds = n
    let res =  seconds === 1 ? `${seconds} second` : `${seconds} seconds`;
    arr.push(res);
  }
  
   
  return arr.length > 2 ? arr.join(", ").replace(/,([^,]*)$/,' and'+'$1') : arr.join(" and ");
}

console.log(formatDuration(3662))
```
