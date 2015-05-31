## Chapter 2: Challenging assumptions

After you have read a problem and understand what it is asking, you will want to begin solving the problem.

Don't do this!

If you jump into solving a problem too early, you may miss key insights or make a bad assumption that will cost you valuable time. In the worst case, a bad assumption will force you to start over!

Challenging assumptions is more difficult than it seems. After reading a problem, you will have a preconceived notion of what you are solving for. Reaching that goal is important, but you don't want to miss something crucial along the way.

For example, suppose an interviewer asks you to find the mean of a list of integers. That sounds simple enough. You add up all the integers and then divide by the total number of values. You test it out on the whiteboard, and it seems to work. The interviewer asks you if you see anything wrong with what you wrote. You don't. The interviewer says, "What if I gave you the list `[INT_MAX, INT_MAX]`?" Aha! You assumed that you would be able to add all the integers without running into overflow. That bad assumption will now force you to start solving the problem again from scratch. Not only that, but you also just gave a clear signal to your interviewer that you are prone to make mistakes.

Avoiding bad assumptions is difficult. Sometimes the best way to avoid making bad assumptions is to learn from experience. However, this chapter aims to provide a few safeguards for the most common bad assumptions.

### Common Bad Assumptions

1. #### Assuming inputs are non-null

 Lots of interview problems have an array, string, or data structure as an input. Will your algorithm break if one of these is null?

 Consider the problem:
 
 >```html
 Write a method to return the mean of a list of integers.
 ```

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

---

Next: [Chapter 3: ???](../Chapter 3/README.md)

