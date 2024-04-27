1. At line 12 the program will print out `3` because if we look closely inside the for loop, at some point i is increased into 3 and the loop no longer continues running because the length of prices is 3 which means i less than prices.length is false. Since i is of var type, it is accessible by line 12.
2. At line 13 the program prints out the final unrodunded price of the last `prices` array element after it has already been calculated in relation to the `discount` argument. Before the loop ends, 150 is stored inside `discountedPrice`, which is the value caught by line 13. Note: since discountedPrice is of var type, then it is accessible by line 13 regardless of the for loop's scope.
3. At line 14 the program will print out the final rounded price of the last `prices` array element given that is has already been calculated by the `discount` variable. In this case the program outputs `150` since `300` was the last array element inside `prices` array and basically before the for loop ends, `finalPrice` stores `150`, which is the value caught by line 14.
4. Nothing gets printed out, but what gets returned is `[ 50, 100, 150 ]`. Basically we get this because our `discountPrices` function works by calculating the total new price for all elements in the array numbers we pass into the function in relation to the discounted price variable we also pass. Every time the program calculates the new price, it is stored inside a new list `discounted`. After the program is done calculating the new prices, the `discounted` array is returned. 
5. We get an error telling us that `i` is not defined. The reason why this occurs is because i is of type `let`, which means that it is only accessible within the scope of the for loop in our case. Since we tried to access it outside of the for loop scope, we get an error since `i` is no longer reachable.
6. We get the same error as question 5 because `discountedPrice` variable is of `let` type meaning that it is not accessible outside of the for loop. 
7. Similar to `question 3`, `150` is printed out because `finalPrice` is of type `let` meaning that it can only be reached inside of the `discountedPrices` function. Since line 14 is inside of that scope, there are no errors involving the use of `let`.
8. Program returns the exact results as `question 4` because the `discounted` variable is of `let` type and can only be accessed anywhere inside `discountedPrices`. Because of that, there were no errors and the program executed identically to what happened in `question 4`.
9. We get an error where `i` is not defined because it was declared as `let` type and since we tried to access it outside of the allowed scope, we get an error saying that `i` was not defined.
10. `3` gets printed out because that is indeed the length of the array that we passed as the first argument to the function. Since `length` is `const` and we never changed it, no errors were present.
11. We get the exact results as `question 4` where `[ 50, 100, 150 ]` is returned. There are no errors because all variables of type `const` were never reassigned and `i` was never invoked outside of its scope. Although a bit confusing, `line 7` seems to reassign the `discountedPrice` variable, but we actually create a new `const discountedPrice` for every iteration, so that is valid.
12. A. `student.name`
    B. `student['Grad Year']`
    C. `student.greeting()`
    D. `student['Favorite Teacher']['name']`
    E. `student['courseLoad'][0]` 

13. A. We get `'32'` because since we have a string, in this case `'3'`, the `+` operator will concatenate `int` 2 into string `'3'` resulting in `'32'`.
    B. We get `1` because the `-` operator is used to convert our variables into `int`. So, we get `3-2` which equals to `1`.
    C. we get `3` because `null` is simply converted to 0 by the `+` operator.
    D. we get `'3null'` because the `+` operator will simply convert `null` into a string since we are trying to use the operator with another string, in this case `'3'`.
    E. we get `4` because `true` is simply converted to its corresponding integer value `1` given that we are using the `+` operator with an integer value. So the addition of 3 plus 1 is 4.
    F. The `+` operator will convert both values into integers, so we have `0 + 0` which equals to our final answer `0`.
    G. we get `'3undefined'` because since we have a string value using the `+` operator, `undefined` gets converted into a string and gets concatenated with '3'.
    H. we get `NaN` because when the `-` operator is used, `undefined` is converted into `NaN` which means 'not a number'. This will result in `NaN` no matter what because a variable minus something that is not a number will results in something that is not real. 

14. A. We get `true` because the `>` operator will convert `2` into an integer. Since `2 > 1` is indeed true, the conditional statement returns `true`.
    B. We get `false` because since we are comparing two strings, we use compare each of their characters and as a result of their `ascii` we know that this statement is indeed `false`.
    C. We get `true` because the `==` operator will convert `2` into an integer due to how we have an integer present in the comparison of the string. Since `2=2` is indeed true, we get `true`.
    D. We get `false` because the `===` operator does not perform type conversions. As a result of different types being present, `false` is returned.
    E. We get `false` because `true` gets converted into `1` and since `1=2` is false, we get `false`.
    F. We get `true` because when we use the `===` we are checking that we get the same type of `true`. When we pass any non-zero number to the function `Boolean(number)` we always get `true` unless a zero is passed. Since `true` and `true` are the same type and value, we get `true`.
15. The difference between `==` and `===` is that `==` automatically performs type coercion if the operand are of different types. In contrast, `===` does not perform any type coersion, so if the operands are of different types JS returns `false` instantly. 
16. completed
17. `[2,4,6]` will be the resulting new array. We first create our constant `newArr` that cannot be reassigned, but modified. We then iterate through each array element of `array` and for each iteration we add the result of invoking `callback(array[i])`, which basically tells the program to call `doSomething(num)` for all elements and lastly push the result into `newArr`. To summarize, the function `modifyArray` receives an array as an argument ,multiplies each element by 2, and returns the new results as a new array.
18. completed
19. code snipped prints in the following order: `1 4 3 2`. Basically line 2 executes instantly, line 3 is scheduled to execute 1 second in the future, line 4 scheduled to execute 0 seconds into the future, but with some minimal delay, and line 5 executes instantly. As a result `1 4` get outputted instantly followed by `3` and then `2`.
