
# DESCRIPTION
>
Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized only if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case). The next words should be always capitalized.
>

# SOLUTION
```javascript
function toCamelCase(str){
  let res=''
  for(let i=0;i<str.length;i++){
    if(str.charAt(i)== '-' || str.charAt(i)=='_' ){
      res+=str.charAt(i+1).toUpperCase()
      i++
    }else{
      res+=str.charAt(i)
    }
  }
  return res
}
```

