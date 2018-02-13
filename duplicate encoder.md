# convert a string to a new string where each character in the new string is 
'(' if that character appears only once in the original string, or ')'
if that character appears more than once in the original string.
```
function duplicateEncode(word){
words = word.toLowerCase().split('');
return words.map(function(i,j)
{
return words.some(function(k,l)
{
 ** return k==i && l!=j
}) ? ')' : '(' 
}).join('')
} **
```
The some() method determines whether at least one element of the array matches the given predicate. 
It only returns false if none of the array elements match the predicate:
