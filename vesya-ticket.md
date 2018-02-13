# Vesya clerk ticket problem
```
function tickets(peopleInLine){
var ticket = "";
  var dollors= 0;
  for (var i = 0; i < peopleInLine.length; i++) {
    if (peopleInLine[i] - 25 > dollors) {
      ticket = "NO";
      break;
    } else {
      dollors = dollors + 25;
      ticket = "YES";
    }
  }
  return ticket
}

```
