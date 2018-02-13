# Replace alphabhet with its position

```
function alphabetPosition(text) {
  positionalpha = text.toLowerCase().split('').filter(c=> c >='a' & c <='z')
  .map(c=> c.charCodeAt(0) - 'a'.charCodeAt(0) + 1 ).join(' ');
return positionalpha;
}
  ```
