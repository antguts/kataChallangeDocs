# DESCRIPTION
>
Complete the solution so that the function will break up camel casing, using a space between words.
>

## EXAMPLE
```
"camelCasing"  =>  "camel Casing"
"identifier"   =>  "identifier"
""             =>  ""
```

# SOLUTION
```javascript
function solution(string) {
  let result = ''
  let start = 0
   
  for(let i=0;i<string.length;i++){
      if(string[i] == string[i].toUpperCase()){
      result += string.slice(start,i)+' '
      start = i
      }
      if(i == string.length-1) result += string.slice(start,i+1)
  }

return result
}
```