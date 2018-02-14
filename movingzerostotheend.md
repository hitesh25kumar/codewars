# Moving zeros to the end of the array

```
var moveZeros = function (arr) {
  for(var i=arr.length;i--;)
{
if(arr[i]===0)
{
arr.splice(i,1);
arr.push(0);
}
}
return arr;
}
```
splice is used to remove 0 from array 
push is used to add zero at end of array
