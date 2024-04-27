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
12. 
    A. `student.name`
    B. `student['Grad Year']`
    C. `student.greeting()`
    D. `student['Favorite Teacher']['name']`
    E. `student['courseLoad'][0]`

    