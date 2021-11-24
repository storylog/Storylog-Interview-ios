**Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.**

**You may assume that each input would have exactly one solution, and you may not use the same element twice.**

**You can return the answer in any order.**

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
-100 < nums[i] <= 100
-1000 < target <= 1000
Only one valid answer exists.
```

Sample Input:
```ruby
input = [3,2,4]
target = 6
```

Sample Output
```ruby
[1,2]
```

Example:

```ruby
// Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
func plusMinus(arr: [Int]) -> [Any]? {
    //...
    //... do something
    //...
    return nil
}

let inputA = [3,2,4], targetA = 6
_ = plusMinus(arr: inputA)
// expected [1,2]

let inputB = [3,3], targetB = 6
_ = plusMinus(arr: inputB)
// expected [0,1]

let inputC = [2,7,11,15], targetC = 9
_ = plusMinus(arr: inputC)
// expected [0,1]

let inputD = [1,5,8,7,11,15,1,50,8,98,47,312,14,20,54,26,16], targetD = 30
_ = plusMinus(arr: inputD)
// expected [12,16]

```
