# DESCRIPTION
>
Can you find a pattern in it? If so, then write a function getScore(n)/get_score(n)/GetScore(n) which returns the score for any positive number n.

Note Real test cases consists of 100 random cases where 1 <= n <= 10000
>

## EXAMPLE
```
 n | score
---+-------
 1 |  50
 2 |  150
 3 |  300
 4 |  500
 5 |  750
```

# SOLUTION
```javascript
function getScore(n) {
  let cnt=0
  let t=50
 
  for(let i=0;i<n;i++){
    cnt+=t
    t+=50
  }
 
 return cnt
}
```