# DESCRIPTION
>
Some numbers have funny properties. For example:
>
```
89 --> 8¹ + 9² = 89 * 1

695 --> 6² + 9³ + 5⁴= 1390 = 695 * 2

46288 --> 4³ + 6⁴+ 2⁵ + 8⁶ + 8⁷ = 2360688 = 46288 * 51
```
>
Given a positive integer n written as abcd... (a, b, c, d... being digits) and a positive integer p

we want to find a positive integer k, if it exists, such that the sum of the digits of n taken to the successive powers of p is equal to k * n.
>


# SOLUTION
```javascript
function digPow(n, p){

  let res=Array.from(String(n), Number).map((i)=>{
    let t= i**p;
    p++;
    return t;
  }).reduce((a, b) => a + b, 0)
  return res%n==0? res/n : -1
} 
```