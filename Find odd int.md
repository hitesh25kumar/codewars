# Find odd number of integer from array
```
function findOdd(A) {
 var number;
 var count = 0;
 for(var i=0;i<A.length;i++)
 {
 var number = A[i];
 for(var a =0;a<A.length;a++)
 {
 if(A[a]==number)
 {
 count++;
 }
 }
 if(count%2!=0)
 {
 return number;
 }
 }
}
```
