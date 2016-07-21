## Chapter 2: Challenging assumptions

After you have read a problem and understand what it is asking, you will want to begin solving the problem.

Don't do this!

If you jump into solving a problem too early, you may miss key insights or make a bad assumption that will cost you valuable time. In the worst case, a bad assumption will force you to start over!

Challenging assumptions is more difficult than it seems. After reading a problem, you will have a preconceived notion of what you are solving for. Reaching that goal is important, but you don't want to miss something crucial along the way.

For example, suppose an interviewer asks you to find the mean of a list of integers. That sounds simple enough. You add up all the integers and then divide by the total number of values. You test it out on the whiteboard, and it seems to work. The interviewer asks you if you see anything wrong with what you wrote. You don't. The interviewer says, "What if I gave you the list `[INT_MAX, INT_MAX]`?" Aha! You assumed that you would be able to add all the integers without running into overflow. That bad assumption will now force you to start solving the problem again from scratch. Not only that, but you also just gave a clear signal to your interviewer that you are prone to make mistakes.

Avoiding bad assumptions is difficult. Sometimes the best way to avoid making bad assumptions is to learn from experience. However, this chapter aims to provide a few safeguards for the most common bad assumptions.

### Common Bad Assumptions

#### Assuming input values have a particular data type

An interviewer might ask something like:

> Implement an efficient data structure that supports `insert()` and `getMedian()`. The `insert()` method should insert a number into the data structure. The `getMedian()` method should return the median of all inserted numbers.

You might go on to write a class that looks like:

```java
public class MedianCollection {
    public void insert(int number) {
        ...
    }
    
    public double getMedian() {
        ...
    }
}
```

The problem here is that you have assumed that all the numbers in the collection are `int` values. The numbers in the collection could potentially be `double` values. The point is that you don't know, so you have to ask your interviewer for more information.

You might ask, "What kind of numbers can be inserted into the data structure? Integers only? Real numbers?"

To avoid making this mistake, learn to identify generic words like *number*. When you hear them, ask for clarification.

Look out for the following generic words in a problem statement:

* **number** -- what kind of number?
* **tree** -- what kind of tree?
* **list** -- what kind of list? an array? a linked list? a resizable array?
* **graph** -- what kind of graph? directed? acyclic?

#### Assuming input values have a particular range

It's common to assume that the input values you are given will lie in some range that makes sense for the problem. For example, maybe you are given a graph with weights on the edges that denote the cost of moving from one node to another. You are asked to find the shortest path between two nodes in the graph, so you apply Dijkstra's algorithm. In doing so, you have made the assumption that edge weights are not negative. Maybe for this particular problem, negative edge weights are valid. Make sure you question the assumptions you make about the range for particular variables. If you are not sure what range a variable might take, ask your interviewer.

It's also common to make this kind of mistake with collections. Many people assume that whatever collection they are working with has enough elements in it. For example, maybe you are asked to find the `k` brightest stars in a list of `n` stars. It's easy to assume that `n >= k` because that's the only way you can arrive at a meaningful solution. However, it's possible that someone will pass an empty list or a list with only three values when `k` is  a larger value, like ten. Make sure the code you write accounts for the possibility that `n < k` by throwing an exception in that case.


#### Assuming you have a binary search tree when only a binary tree is specified

A common mistake is to assume that you have a binary search tree when the interviewer says "binary tree." The best way to avoid this mistake it to listen carefully to what the interviewer says.

You can solve lots of problems more efficiently if you are given a binary search tree, so it is tempting to assume that you have one. For instance, consider the problem of finding the lowest common ancestor of two nodes. If you are given a (balanced) binary search tree, the problem can be solved in `O(lg n)` time. If you are given a regular binary tree, the problem can be solved in `O(n)` time. Don't let the fact that you've heard a problem before tempt you into making quick assumptions.

#### Assuming inputs are non-null

Lots of interview problems have an array, string, or data structure as an input. Will your algorithm break if one of these is null?

Consider the problem:
 
> Write a method to return the mean of a list of integers.

If you start off with:
 
```java
public static double findMean(int[] numbers) {
    int n = numbers.length;
    ...
}
```
 
Then you've already made a mistake. If `numbers` is null, your program will throw an exception.
 
You can ask the interviewer what the expected result is supposed to be when you are passed `null`. If the interviewer leaves the choice up to you, you can throw an exception or you can return a canned value, e.g.:
 
```java
public static double findMean(int[] numbers) {
    if (numbers == null) {
        throw new IllegalArgumentException("Cannot find the mean of null array!");
    }
     
    int n = numbers.length;
    ...
}
```

or
 
```java
public static double findMean(int[] numbers) {
    if (numbers == null) {
        return 0;
    }
     
    int n = numbers.length;
    ...
}
```

#### Assuming an input collection has at least `k` items

---

Next: [Chapter 3: ???](../Chapter 3/README.md)

