### Highest Common Factor 
```js

//get H.C.F value 
function getHeightCommonFactor(...numbers){
    let commonFactors = getCommonFactors(...numbers);
    return Math.max(...commonFactors);
}


//get common factors code 
function getCommonFactors(...numbers){
    numbers = numbers.map((number) => getFactors(number));

    return numbers[0].filter(function (factor){
        let match = true;
        for(let i = 0; i < numbers.length; i++){
            if (!numbers[i].includes(factor)){
                match = false;
                break;
            }
        }
        return match
    })
}


//get factors
function getFactors(num) {
    const factors = [];
    for (let i = 1; i <= Math.sqrt(num); i++) {
        if (num % i === 0) {
            let result = num / i; //ভাগফল 
            factors.push(i);
            factors.push(result);
        }
    }
    let uniqueFactors = Array.from(new Set(factors));
    //Assending Sort 
    return uniqueFactors.sort();
}
```