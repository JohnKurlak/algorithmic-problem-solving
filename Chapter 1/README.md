## Chapter 1: Understanding the problem

Algorithmic interview problems tend to follow a particular format. Being familiar with this format is necessary for solving problems quickly and correctly.

Consider the following problem statement:

> You have a catalog of stars, with each star stored as an object of the following class:

>```java
class Star {
    String name;
    int brightness;
    ...
}
```

> Write a method that accepts an array of `n` stars and an integer `k` and returns the `k` brightest stars.

### Identifying the goal of a problem

The first time you hear a problem statement, try to identify the basic goal of the problem. Do this by looking for verbs that command you to do something.  Common verbs in problem statements include:

* Find
* Determine
* Minimize/maximize
* Count
* Calculate
* Return
* Design

...and so on.

If you still don't understand what a question is asking after hearing it, ask your interviewer to clarify.

Once you know what the problem is asking, you will be better prepared to analyze the other components of the problem.

### Understanding the terminology

Now that you know what your goal is, it's time to break the problem down into its individual parts. To do that, you must first understand the terminology used in interview problems.

Many interview problems use specific terminology for:

* Variables and their ranges
* Run-time complexity and space complexity
* Math and programming concepts

#### Variables and their ranges

Interview problems use variables to specify quantities whose values are unknown until run-time. This means variables are handy for specifying inputs and outputs.

Generally, variables are expressed as a single lowercase or uppercase letters from either the English alphabet (e.g., a, b, c, ...) or the Greek alphabet (e.g., α, β, γ, ...).

In the example problem above, we have two variables: `n` and `k`.

`n` represents the number of stars that we are given.
`k` represents the number of stars that we should return.

#### Run-time complexity and space complexity

Sometimes an interviewer will impose a restriction on run-time complexity or space complexity. These restrictions are usually written in Big O notation.

If you are not familiar with Big O notation, please see [Appendix A: Big O Notation](../Appendix A/README.md).

#### Math and programming concepts

There are a number of math and programming concepts that show up in interview problems. Knowing the meaning of these concepts will help you better understand technical interview problems.

Here are some common math and programming terms used in interview problems:

* subarray
* substring
* subsequence
* maximum
* minimum
* lexicographical
* permutation
* combination
* recursive
* iterative
* frequent
* common
* prime number

And many more...

Refer to the [glossary](../GLOSSARY.md) for definitions and examples.

### Identifying inputs and outputs

At this point, you should understand what the problem is asking. Next, your goal is to identify the inputs and outputs for the problem.

Being able to identify variables in a problem is crucial to being able to identify inputs and outputs.

#### Identifying inputs

Inputs are variables that influence the resulting output for a problem. Therefore, to identify inputs, look at all values that you are given for a problem. For each value, ask yourself, "Could changing this value result in a different output?" If the answer is "Yes," then you have identified an input!

Consider the example problem above. We are given an array of `n` stars and an integer, `k`. If we change the collection of stars, then we certainly will get a different output. Further, if we change how many stars we want to output, then we also will get a different output.  Therefore, both the collection of stars and the value `k` are inputs.

#### Identifying outputs

Outputs are variables whose values depend on the inputs. Usually, a problem will have a single output, and that output is the answer to the problem.

In the example problem above, the output is a collection of the `k` brightest stars.

---

Next: [Chapter 2: Challenging assumptions](../Chapter 2/README.md)