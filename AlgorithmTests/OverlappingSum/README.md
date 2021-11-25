**Given two arrays of integers. Write a program to find the sum of all the overlapping elements between two arrays. If any element is found to overlap, that element will not be recalculated.**

Constraints:
```ruby
0 < n <= 100
-100 < arr[i] <= 100
```

Sample Input:
```ruby
inputA = [1, 5, 3, 8]
inputB = [5, 4, 6, 7]
```

Sample Output
```ruby
10
```

Example:

```ruby
func findSum(input1: [Int], input2: [Int], n: Int) -> Any? {
    //...
    //... do something
    //...
    return nil
}

/* Input A */
let inputA1 = [1, 5, 3, 8]
let inputA2 = [5, 4, 6, 7]
_ = findSum(input1: inputA1, input2: inputA2, n: 4)
// expected == 10

/* Input B*/
let inputB1 = [1, 5, 3, 8]
let inputB2 = [5, 1, 8, 3]
_ = findSum(input1: inputB1, input2: inputB2, n: 4)
// expected == 34

/* Input C*/
let inputC1 = [1, 2, 3, 4]
let inputC2 = [5, 8, 8, 7]
_ = findSum(input1: inputC1, input2: inputC2, n: 4)
// expected == 0

/* Input D */
let inputD1 = [1, 5, 5, 5]
let inputD2 = [5, 4, 5, 7]
_ = findSum(input1: inputD1, input2: inputD2, n: 4)
// expected == 20
```
