# **Tribonacci | Codewars** #

#### Christian Glassiognon | Javascript ####  

## **Introduction** ##

The [tribonacci kata](https://www.codewars.com/kata/556deca17c58da83c00002db) takes the [fibonacci sequence](https://www.mathsisfun.com/numbers/fibonacci-sequence.html) and adds toghether 3 numbers instead of two.

There is no solution for this problem in the JS Library so we will implement it ourselves.

Additionally, this function is implemented iteratively for simplicity, however it can also be made recursively similar to a fibonacci function.

We will solve this problem by adding the last three numbers in the array and then adding this number to the end of the array. The one exeption to this is if ***n*** is less than 3, in that case we will add ***n*** numbers from the ***signature*** array to the ***answer*** array.

### *Tribonacci Example* ###
##### [Tribonacci Kata Instructions](https://www.codewars.com/kata/556deca17c58da83c00002db) #####

    [1, 1 ,1, 3, 5, 9, 17, 31, ...]

### *Function Signature* ###

    function tribonacci(signature, n)
    
    /*signature (array): first 3 numbers to start sequence
    n (number): number of items in return array*/

### *Return value* ###
An array of tribonacci numbers

## Code ##

Written with [Conditional(Ternary) operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

    function tribonacci(signature, n) {
        let answer = [];
        for (let i =0; i < n; i++) {
            let end = answer.length;
            (i<3) ? answer[i] = signature[i] : answer.push(answer[end-1]+answer[end-2]+answer[end-3]);
        }
        return answer;
    }

Written with regular if/else statement

    function tribonacci(signature,n) {
        let answer = [];
        for (let i = 0; i < n; i++) {
            if (i < 3) {
                answer[i] = signature[i];
            } else {
                let end = answer.length;
                answer.push(answer[end-1]+answer[end-2]+answer[end-3]);
            }
        }
        return answer;
    }

##### Hope this guide helps, if you have any suggestions, create a pr request! #####