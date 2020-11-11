---


---

<h1 id="exercise-9">Exercise 9</h1>
<p>Watch the video explaining the rules of the Towers of Hanoi. Implement a recursive method that outputs the correct minimal move set for n disks. Hint: When moving around the n-1 smallest disks, as far as they’re concerned its as though the largest disk does not exist.</p>
<pre><code>public class Hanoi {
	
	public static void printInstructions(int start, int spare, int end, int disks) {
		if(disks == 1) {
			System.out.println("Move from Peg " + start + " to Peg " + end + ".");
		}
		else {
			// Move the triangle to the spare peg
			printinstructions(start, end, spare, n-1);
			// Move the largest disk to the end
			printInstructions(start, spare, end 1)
			// Move the triangle from the spare to the end
			printInstructions(spare, start, end n-1)
		}
	}
}
</code></pre>
<p>Consider our implementation of MyStack from a few weeks ago. Write a method which mutates the stack by removing the “bottom” element from it. This should be done recurively using only pop, push, and top. You should no be accessing the array directly.</p>
<p>In RecLLUtil, change the removeAll method so that it also works when the first element should be deleted. Hint: Consider writing a “shift forward” method. Write this method recusivly.</p>
<p>In RecLLUtil, implement a recursive “contains” method.</p>
<p>Change the methods in our LinkedList to be implemented recursively. Hint: you may need to write recursive “helper methods” indtead of making the methods directly recursive.</p>
<p>Imagine you have a Set data structure with the following functionalities:</p>
<ol>
<li>Union: Takes in two Sets and returns their union</li>
<li>Add element to each: Takes in a Set of type Set called S (S is a set of sets of type T), and an element e of type T, returns a modified version of S such that e is added to every element of S.</li>
</ol>
<p>How might you implement a method which takes in a Set, and returns it’s power set? Don’t worry too much about Java specific implementation details. But rather, focus on the algorithm.</p>

