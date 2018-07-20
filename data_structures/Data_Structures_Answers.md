Add your answers to the questions below.

1. What is the runtime complexity of your `depth_first_for_each` method?
O(n)
2. What is the space complexity of your `depth_first_for_each` function?
O(1)
3. What is the runtime complexity of your `breadth_first_for_each` method?
O(n)
4. What is the space complexity of your `breadth_first_for_each` method?
O(logn), however it also iterates over each element twice during the function, making the overall complexity equal to O(n)
5. What is the runtime complexity of your `heapsort` function?
it uses bubble up and sift down implicitly which are both O(logn)
6. What is the space complexity of the `heapsort` function? Recall that your implementation should return a new array with the sorted data. What would be the space complexity if your function instead altered the input array?
my space complexity is O(n). If the function altered the input array, it would need O(1) space beyond the input array
