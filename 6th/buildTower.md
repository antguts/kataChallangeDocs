# DESCRIPTION
>
Build a pyramid-shaped tower, as an array/list of strings, given a positive integer number of floors. A tower block is represented with "*" character.

For example, a tower with 3 floors looks like this:
>
```
[
  "  *  ",
  " *** ", 
  "*****"
]
```

# SOLUTION
```javascript
function towerBuilder(nFloors) {
  let arr=[]
  let star=1
  let tt =nFloors

  
  for(let i=0;i<nFloors;i++){
    arr.push(` `.repeat(tt-1)+'*'.repeat(star)+' '.repeat(tt-1))
    tt-=1
    star+=2
  }
  
  return arr
}
```