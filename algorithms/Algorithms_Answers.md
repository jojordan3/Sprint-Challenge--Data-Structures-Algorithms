because Aaron made the pseudocode "**very** close to minimal java" as he said, ~~I'm rebelling and using python notation for my exponents!~~ So I wanted to do that until I realized that two asterisks mark bold... BUT know the sentiment is there! :P

Exercise I
a. O(n) because the math essentially comes down to (n^3)/(n^2)
b. O(n) because worst case is every element is greater than x so you're iterating just by dividing n by 2->linear
c. O(n^(1/2)) because n only appears in the initial iterator (so the sub-iterators (is that a thing?) run in constant time WRT n) and we take the square root of n then count up to it
d. O(nlogn) the first for loops runs O(logn) over the second which runs O(n).
e. O(n^3) for similar reasons as d
f. O(n) each step in the recursion counts down from n until it reaches 0
g. O(n) just searching through the array one by one

Exercise II
a. create 2 additional arrays of same size as original arr, n elements: LMin and RMax
LMin[0] = arr[0]
i = 1
while i < n:
  LMin[i] = min(arr[i], LMin[i - 1])
  i += 1
  
RMax[n - 1] = arr[n - 1]
j = n - 2
while j >= 0:
  RMax[j] = max(arr[j], RMax[j + 1])
  j -= 1

max_diff = -inf
for index in range(len(arr)):
  max_diff = max(RMax[index] - LMin[index], max_diff)
  index += 1
    
b. throw of story n/2.
      if it breaks, throw of story n/4
      if it doesnt break, throw off story 3n/4
          keep going, dividing the available space for f by 2 each time, moving to the upper half if it doesn't break and lower half if it does
          

Exercise III
a. O(n^2) because the remaining array to be sorted only decreases by 1 with each pass so it will be called n times, and each time it will have n items to interact with.
b. O(nlogn) because we reduce the number of items in the arrays to be sorted by half each time, so it will take logn iterations to finish down one "branch". In each branch level of the tree, each of the n items will be compared
