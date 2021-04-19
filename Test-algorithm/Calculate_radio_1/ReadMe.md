**Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero.**

**Example:**

**arr = [-1, -1, 0 , 1, 1]**

**there are n = 5 elements, two positive, two negative and one zero. their ratios are `2/5 = 0.400000 , 2/5 = 0.400000, 1/5 = 0.200000` Results are printed as: **
```ruby
0.400000 
0.400000
0.200000
```

Constraints:
```ruby
0 < n <= 100
-100 < arr[i] <= 100
```

Output Format:
Print the following 3 lines,
```ruby
1. proportion of positive values
2. proportion of negative values
3. proportion of zeros
```

Sample Input:
```ruby
input1 = [-1, -1, 0 , 1, 1]
input2 = [-4, 3, -9, 0, 4, 1]
```

Sample Output
```ruby
0.500000
0.333333
0.166667
```

Example:

```ruby
func plusMinus(arr: [Int]) -> [Any]? {
    //...
    //... do something
    //...
    return nil
}

let input1 = [-1, -1, 0 , 1, 1]
_ = plusMinus(arr: input1)

let input2 = [-4, 3, -9, 0, 4, 1]
_ = plusMinus(arr: input2)
```
