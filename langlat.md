# Coordinates validator
## Validates longitutde and lattitude
```
function isValidCoordinates(coordinates){
  
  var coordReg = /^(-?\d+(\.\d+)?),\s*(-?\d+(\.\d+)?)$/g
  if (!coordReg.test(coordinates)) {
    return false;
  }
  
  var arrCoordinates = coordinates.split(',');
  try {
    var latstr = arrCoordinates[0].trim();    
    var lat = parseFloat(latstr);
    if (lat < -90 || lat > 90) { return false; }
  } catch (e) {
    console.log(e);
    return false;
  }
  
  try {
    var lngstr = arrCoordinates[1].trim();    
    var lng = parseFloat(lngstr);
    if (lng < -180 || lng > 180) { return false; }
  } catch (e) {
    return false;
  }
  
  return true; 
}
```
coordReg is usedv to validate that a longitude and lattidude is valid or not
trim function is used to remove whitespace from both sides of a string.
lattitude can be between 0 and 90, positive or negative.
longitude can be between 0 and 180, positive or negative.
