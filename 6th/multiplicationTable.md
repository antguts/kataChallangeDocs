# DESCRIPTION
>
Your task, is to create NxN multiplication table, of size provided in parameter.

for example, when given size is 3:
>
```
1 2 3
2 4 6
3 6 9
```

# SOLUTION
```javascript
multiplicationTable = function(size) {
  var res = [];
  let cnt=1
  
  for(let i=0;i<size;i++){
    let temp=[]
    for(let j=0;j<size;j++){
      temp.push(cnt*(j+1))
    }
    res.push(temp)
    cnt++;
  }
  return res
}
```