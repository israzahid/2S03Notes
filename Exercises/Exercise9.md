---


---

<h1 id="exercise-9">Exercise 9</h1>
<ol>
<li>
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
</li>
<li>
<p>Consider our implementation of MyStack from a few weeks ago. Write a method which mutates the stack by removing the “bottom” element from it. This should be done recursively using only pop, push, and top. You should not be accessing the array directly.</p>
<pre><code>	public int getHeight() {
		if (isEmpty()) {
			return 0;
		}
		int top = pop();
		int temp = 1 + getHeight();
		push(top);
		return temp;
	}

	public void removeBottom() {
		if (height == 1) {
			pop();
		}
		else {
			int temp = pop();
			removeBottom();
			push(temp);
		}
	}
</code></pre>
</li>
<li>
<p>In RecLLUtil<br>
a. change the removeAll method so that it also works when the first element should be deleted. Hint: Consider writing a “shift forward” method. Write this method recursively.<br>
b. In RecLLUtil, implement a recursive “contains” method.</p>
<pre><code>public static boolean contains(RecLL L, int value) {
	if (L.isEmpty()) {
		return false;
	}
	if (L.value == value) {
		return true;
	}
	if (L.next == null) {
		false
	}
	else {
		return contains(L.next, value);
	}
}
</code></pre>
</li>
<li>
<p>Change the methods in our LinkedList to be implemented recursively. Hint: you may need to write recursive “helper methods” instead of making the methods directly recursive.</p>
</li>
<li>
<p>Imagine you have a Set data structure with the following functionalities:</p>
</li>
</ol>
<ol>
<li>Union: Takes in two Sets and returns their union</li>
<li>Add element to each: Takes in a Set of type Set called S (S is a set of sets of type T), and an element e of type T, returns a modified version of S such that e is added to every element of S.</li>
</ol>
<p>How might you implement a method which takes in a Set, and returns it’s power set? Don’t worry too much about Java specific implementation details. But rather, focus on the algorithm.</p>
<ul>
<li>if the set is empty, return empty set: {}</li>
<li>take the first element of the set into another variable
<ul>
<li>element = set[0];</li>
</ul>
</li>
<li>remove that element
<ul>
<li>set.remove(element);</li>
</ul>
</li>
<li>return the (power set of S) in union with (power set of S, adding the removed element)
<ul>
<li>return PS(set).union.PS(S)addToEach(element);</li>
</ul>
</li>
</ul>

