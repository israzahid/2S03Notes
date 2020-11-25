---


---

<h1 id="exercise-11">Exercise 11</h1>
<ol>
<li>This question is not on testable material directly, but it will help you understand the worth of BSTs. Imagine you need to insert the numbers 1-5 into a BST. How many different ways could you insert these numbers to generate a BST which has height 5? Draw these trees out (or draw some of them if you think there are too many to draw).</li>
</ol>
<pre><code>1					5	1			1			5		1
 \				   /	 \ 			 \		   /		 \ 
  2	       	      4		  2			  5	      4			  5
   \		     /		   \		 /		 /			 /
    3		    3			3		2		2			4
     \		   /			 \		 \		 \		   /	
      4		  2				  5		  4		  3		  2	
	\	 /				 /		 /		 /		   \
	  5	1				4		3		1			3
</code></pre>
<ul>
<li>to generate worse case, put numbers in a line and take one off most extreme ends
<ul>
<li>it does not matter which side taken off of as long as it is on the sides</li>
</ul>
</li>
</ul>
<p>a. Now what bout inserting the numbers 1-n, how many BSTs with height n exist then?<br>
<code>(n - 1)^2</code></p>
<ol start="2">
<li>Use a BST to write a method which given an array of integers, prints them out to the console in ascending (sorted) order.</li>
</ol>
<pre><code>public static void treeSort(int[] values) {  
	BST tree = new BST();  
	for(int value: values) {  
		tree.insert(value);  
	}  
	tree.printInOrder();  
}
</code></pre>
<ol start="3">
<li>What if we choose to instead put larger values to the left, and smaller values to the right? Do we still get all the advantages of a BST? Write a method, which “mirrors” a given BST. For example, it would change</li>
</ol>
<pre><code>        4                      4
      /   \       -&gt;         /   \
     1     6                6     1
          / \              / \
         5   8            8   5
</code></pre>
<pre><code>public void mirror() {  
	if(isLeaf()) {  
		return;
	}  
	else if(!hasLeftChild()) {  
		left = right;
		right = null;  
		left.mirror();  
	}  
	else if(!hasRightChild()) {  
		right = left;  
		left = null;  
		right.mirror();  
	}  
	else {  
		BST temp;  
		temp = left;  
		left = right;  
		right = temp;  
		left.mirror();  
		right.mirror();  
	}  
}
</code></pre>
<ol start="4">
<li>Rewrite the BST code so that it is encapsulated in another class. Similar to the LL implementation where we had a pointer to head (it will be root in this case). Can we still write methods recursively?</li>
</ol>
<p><code>Node.java</code></p>
<pre><code>public class Node() {
	int value
	Node right;
	Node left;

	public Node(int value) {
		this.value = value;
	}
}
</code></pre>
<p><code>BST.java</code></p>
<pre><code>public void insert(int value) {
	insertRec(root, value);
}

public void insertRec(Node node, int value) {
	// Base cases
	if (value &lt; node.value) {
		insertRec(node.left, value);
	}
	else {
		inserRec(node.right, value);
	}
}
</code></pre>
<ol start="6">
<li>Implement a BST with delete functionality, as seen in the videos.</li>
</ol>

