# DESCRIPTION
>
Create a function that returns a christmas tree of the correct height.

For example:

height = 5 should return:
>

```
    *    
   ***   
  *****  
 ******* 
*********
```

# SOLUTION
```javascript
function christmasTree(height) {
  let tree = ''
  let cnt=1
  
  for(let i=1;i<=height;i++){
    let end = (height==i || height == 1)? '' : '\n'
    tree += ' '.repeat(height-i) + '*'.repeat(cnt)+' '.repeat(height-i)+ end
    cnt+=2
  }

  return tree
}
```