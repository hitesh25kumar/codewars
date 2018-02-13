# Counting duplicates letters in string

```
function duplicateCount(text){
  var textarr = text.toLowerCase().split('');
  var textobj = textarr.reduce(function(previous,current)
  {
   previous[current] = previous[current] + 1 || 1;
   return previous;
  },{});
  var count =0;
  for(var keys in textobj)
  {
  if(textobj[keys]>1)
  {
   count++;
  }
  }
  return count;
}
```

The reduce() method executes a provided function for each value of the array (from left-to-right).
