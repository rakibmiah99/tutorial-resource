### Lowest Common Multiple(L.C.M) বা ল.সা.গু 
https://www.youtube.com/watch?v=b1ZV2VzNqAo

https://www.youtube.com/watch?v=utZcJ0leZ_g

```js
//or 
function gcd(a, b){
    if(b == 0){
        return a; 
    }
    return gcd(b, a%b);
}

```

```js
function gcd(a, b) {
    while (b !== 0) {
        let temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

// উদাহরণস্বরূপ ব্যবহার
const number1 = 48;
const number2 = 18;
console.log(`GCD of ${number1} and ${number2} is:`, gcd(number1, number2)); // Output: GCD of 48 and 18 is: 6
```

**ল.সা.গু বের করার সূত্রঃ**

    lcm ফাংশনটি দুটি সংখ্যার LCM নির্ধারণ করে GCF ব্যবহার করে। উপরে উল্লেখিত সূত্র ব্যবহার করা হয়:

    LCM(a,b) = (a×b) / GCF(a,b)

```js

//Get Lowest Common Multiple
function getLowestCommonMultiple(...numbers){
    let gcf = getHeightCommonFactor(...numbers)
    let total_of_numbers_by_multiply = numbers.reduce((acc, val) => acc * val);
    return total_of_numbers_by_multiply / gcf;
}

//Get Height Common Factors
function getHeightCommonFactor(...numbers){
    let commonFactors = getCommonFactors(...numbers);
    return Math.max(...commonFactors);
}

//Get Common Factors 
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


//Get Factors 
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