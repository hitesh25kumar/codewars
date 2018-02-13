# Find longest string consisting of k consecutive string

```
function longestConsec(strarr, k) {
    if(strarr.length===0 || k> strarr.length-1 || k === undefined || k<1 ) return "";
    var maxlength =0;
    var maxvariable;
    for(var i=0;i<strarr.length;i++)
    {
    var str="";
    for(var j=i;j<k+i && j<strarr.length;j++)
    {
    str += strarr[j];
    }
    if(str.length > maxlength)
    {
    maxlength = str.length;
    maxvariable = str;
    }
    }
    if(maxvariable === undefined)
    {
    return "";
    }
    else{
    return maxvariable;
    }
}
```
