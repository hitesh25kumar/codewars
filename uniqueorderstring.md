# Unique in order alphabets of string
```
var uniqueInOrder = function(iterable){
  var uniquekey= [];
  var emptystr = ' ';
  for(i=0;i<iterable.length;i++)
  {
  if(iterable[i] !== emptystr)
  {
  emptystr = iterable[i];
  uniquekey.push(emptystr);
  }
  }
  return uniquekey;
}
```
The push() method adds new items to the end of an array, and returns the new length.
