# Count smily face
```
function countSmileys(arr) {
var smiles = [":)",";)",":-)",";-)",";~)",":~)",":D",";D",":-D",":~D",";-D",";~D"];
var count =0;
for(var i=0;i<arr.length;i++)
{
for(var j=0;j<smiles.length;j++)
{
if(arr[i] ===smiles[j])
{
count++;
}
}
}
return count;
}
```
