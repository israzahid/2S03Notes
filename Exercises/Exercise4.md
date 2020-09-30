# Exercise 4

1) For each of the following loops how many times is STATEMENT approximately run. Give your answer in terms of n. 
```
for(int i = 0; i < n; i = i + 2){
	STATEMENT;
}
```
Answer: `n/2`
```
for(int i = 0; i < n; i = i * 2){
	STATEMENT;
}
```
Answer: `infinite` because of `i = 0`

```
for(int i = 0; i < n; i++){
	for (j = 0; j < n; j++){
		STATEMENT;
	}
}
```
Answer: `n^2`
- the inner loops is called n times and the outer loop runs n times

```
for(int i = 0; i < n; i++){
	for (j = 0; j < n; j = j * 2){
		STATEMENT;
	}
}
```

```
for(int i = 0; i < n; i++){
	for (j = i; j < n; j = j++){
		STATEMENT;
	}
}
```
Answer: `total = n + (n - 1) + (n - 2) + ... + 1 = n(n + 1)/2`
2. In the videos we saw a method similar to below:

	public static void nested(int outer, int inner) {
		for(int i = n; i < outer; i++) {
			for(int j = m; j < inner; j = j + i + n) {
				System.out.println("i = " + i + ", j = " + j + ");
			}
		}
	}

What would be the output of this code if:
n = 2
m = 3
outer = 10
inner = 7

What would the value of n, m, inner, and outer be to output:
i = 3, j = 2
i = 3, j = 8
i = 4, j = 2

3. Why do arrays need to know their length ahead of time? It seems like a disadvantage... but is there an advantage? How do you think "lookups" work? Note, a lookup is when you ask the system what a[i] is. Hint: when we have a 10000 length array, we want a[5000] and aa[15] to evaluate relatively quickly. We'll talk about how exactly arrays are stored in memory in lecture.

- needs to allocate memory ahead of time
&nbsp;
- creates 'addressses' for where each data value will be stored
- contiguous, it's easier to find an address very quickly because it is already located
- without the contiguous structure, you have to iterate through everything to reach an address
- summary: easy and fast lookups

4. We've been using arrays since the first week of this course. Where? How?

5. Do some research on java.util.Arrays. You'll find that in the videos we reinvented the wheel on a few methods. What are they? 

Sorting

&nbsp; a. In the videos we saw how to implement selection sort on an arry. Do some research on different sorting algorithms. Try implementing a few. Some may be too complicated for your current knowledge (don't worry we'll get there). But you should at least be able to implement insertion sort and bubble sort. Trace through your implementations, what are the worst case number of comparisons and swaps that you must make. Do the same thing with selection sort. In general these sorting aglorithms are considered bad, but do they offer any advantages? Are there contexts where one might consider using them?
