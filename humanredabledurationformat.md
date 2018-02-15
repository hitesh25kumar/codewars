# Convert seconds into Human redable duration format minute , hours and seconds

```
function formatDuration (seconds) {

	 var minutes = 0; var hours = 0; var days = 0; var years = 0; 

	if (seconds === 0){
		return "now";
	}
	
	else if (seconds === 1){
		return "1 second";
	}
	
	else if (seconds < 60){
		return seconds + " seconds"; 
	}
	
	if (seconds >= 60){
		minutes = (seconds - seconds % 60) / 60;
		seconds  = seconds - (minutes * 60); 
	} 
	
	if (minutes >= 60){
		hours = (minutes - minutes % 60) / 60;
		minutes = minutes - (hours * 60); 
	}
	
	if (hours >= 24){
		days = (hours - hours % 24) / 24; 
		hours = hours - (days * 24); 
	}
	
	if (days > 365){
		years = (days - days % 365) / 365;
		days = days - (years * 365); 
	}
	
	var durationArr = [];   
	var unitNames = ["years", "days", "hours", "minutes", "seconds"]; 
	var unitNums = [years, days, hours, minutes, seconds]; 
	
	for (var i in unitNums){
		if (unitNums[i] !== 0){
			if (unitNums[i] === 1){ 
				durationArr.push(unitNums[i] + " " + unitNames[i].slice(0, -1) + ", ");
			} else {
				durationArr.push(unitNums[i] + " " + unitNames[i] + ", "); 
			}
			
		}
		
	}
	
	var length = durationArr.length; 
	
	if (length === 1){
		return durationArr[0].slice(0, -2); 
	}
	
	
	
	var lastUnit = durationArr[durationArr.length - 1];
	var secondLastUnit = durationArr[durationArr.length - 2];
	var newLastUnit = " and " + lastUnit.slice(0, -2); 
	var newSecondLastUnit = secondLastUnit.slice(0, -2); 
	durationArr.splice(length - 2, 2, newSecondLastUnit, newLastUnit); 
	var duration = durationArr.join(""); 
	
	return duration; 

}
```

splice is used to add or remove elements from array
splice(-2,2)
remove last 2 elements and add last 2 elements with newlast element and new second last element
that includes and

if length of duration array is 1 that means it has only 1 element like 
1 minutes replace with 1 minute
using slice (0,-2)
