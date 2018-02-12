# Square every digit of an array
```
function squareDigits(num){
  var i,square=[],n;
  num = num.toString();
  for(i=0;i<num.length;i++)
  {
  n = Number(num[i]);
  square.push(n*n);
  }
  return Number(square.join(""));
}
```
The push() method adds new items to the end of an array, and returns the new length.
 The join() method joins the elements of an array into a string, and returns the string.
 The Number() function converts the object argument to a number that represents the object's value.
