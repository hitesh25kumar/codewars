# Square into square (protect trees)

```
function decompose(n) {
 var result = decomposefn(n,n*n)
return result == null ? null : result.slice(0,result.length-1);

}
function decomposefn(n,remain)
{
if(remain == 0)
{
return [n];
}
for(var i=n-1;i>0;i--)
{
if((remain - i*i)>=0)
{
var r = decomposefn (i,(remain - i* i));

if(r!=null)
{
r.push(n);
return r;
}
}
}
}

```

line 6 check wether result is null return it
otherswise check whats remaining

line 9 decomposefn is used to check for remaining parameteres like 1^ 2^ 3^
if nothing remains return n

call decomposefn each time using a loop if to check what is remaining and store the value in r
check if r is not null push the result and return it.
