# Format a string of names like 'Bart, Lisa & Maggie'.
```
function list(names){
 return names.map(function(x){
return x.name;
}).join(", ").replace(/,(?!.*,)/gmi ," &");
}

```
used map function to create a new array and store values according to the function.
used join to join a , after every string.
used gmi for a global multiline case-insensitive search.
used /, to match a , and ?!.* followed by nothing 
used replace function to replace , with &
