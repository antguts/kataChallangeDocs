# DESCRIPTION
>
Assume "#" is like a backspace in string. This means that string "a#bc#d" actually is "bd"

Your task is to process a string with "#" symbols.
>
```
"abc#d##c"      ==>  "ac"
"abc##d######"  ==>  ""
"#######"       ==>  ""
""              ==>  ""
```

# SOLUTION
```javascript
function cleanString(s) {
	let res = []
    
    s.split('').forEach(element=>{
        (element != '#')?
        res.push(element)
        :
        res.pop()
    })
    
  return res.join('')
};
```