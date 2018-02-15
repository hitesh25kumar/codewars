# reverse polish notation calculator

```
function calc(str) {
	
	if (str === ""){
		return 0; 
	}
	
	var polishNotationArr = str.split(" "); 
	var noOperators = true; 
	for (var i = 0; i < polishNotationArr.length; i++){
		if ("+-*/".indexOf(polishNotationArr[i]) > -1){
			noOperators = false; 
		}
	}
	
	if (noOperators){
		return parseFloat(polishNotationArr[polishNotationArr.length - 1]); 
	}
	
	function findNextOperator(arr){
		for (var i = 0; i < arr.length; i++){
			var toEvaluate = ""; 
			var evaluated = "";  
			if ("+-*/".indexOf(arr[i]) > -1 && "+-*/".indexOf(arr[i-1]) === -1 && "+-*/".indexOf(arr[i-2]) === -1 ){
				toEvaluate += arr[i-2] + arr[i] + arr[i-1];
				evaluated = eval(toEvaluate).toString(); 
				arr.splice(i-2, 3, evaluated); 
				findNextOperator(arr);  
			}
		}
		return parseFloat([...arr]); 
	}
	return findNextOperator(polishNotationArr); 
}
```
indexof is used to get the position of an element
evalute means what needs to be evaluated
evaluated means it is evaluated (converted to a string)

