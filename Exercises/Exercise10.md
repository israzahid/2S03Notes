---


---

<h1 id="exercise-10">Exercise 10</h1>
<ol>
<li>In the video we saw an “inorder” traversal. Do some research on preoder and postorder traversals. Implement them.</li>
</ol>
<pre><code>In Order - L P R
public void printInOrder(treeNode head) {
	if (head = null) return;

	printInOrder(head.left);
	System.out.println(head.value);
	printInOrder(head.right);
	
}
</code></pre>
<pre><code>PreOrder - P L R
public void printPreOrder(treeNode head) {
	if (head = null) return;
	
	System.out.print(head.value);
	printPreOrder(head.left);
	printPreOrder(head.right);
}
</code></pre>
<pre><code>PostOrder - L R P
public void printPostOrder(treeNode head) {
	if (head = null) return;

	printPostOrder(head.left);
	printPostOrder(head.right);
	System.out.println(head.value);
	
}
</code></pre>
<ol start="2">
<li>Instead of adding elements to the BinTree manually, create an insert(value) method. What choices do you need to make? What if you wanted to make sure the height of the tree was minimized? How might you implement it then?</li>
</ol>
<ul>
<li>Want to keep it relatively balanced, ensures height of tree is minimized</li>
<li>Two possible implementations:
<ul>
<li>using a random variable to determine if it will go left or right
<ul>
<li>this could lead to a worse case but very rare</li>
<li>very fast and easy to implement</li>
</ul>
</li>
<li>check which side of the root is larger
<ul>
<li>more practical and less random</li>
<li>takes longer because of needing to calculate the height as well</li>
</ul>
</li>
</ul>
</li>
</ul>
<ol start="3">
<li>How would you delete a node from a binary tree. What potential difficulties are there?</li>
</ol>
<ul>
<li>Cases where the node is a leaf, the parent now must just point to a null value</li>
<li>If the node has one side null (left or right), the parent of the node to be deleted will now point to its child</li>
<li>The difficult occurs when the node has two children. There is a solution if the tree was a binary search tree</li>
</ul>
<ol start="4">
<li>Imagine your tree contains integers, and you wish to have fast “lookups”. That is, you wish to be able to determine if a value is in the tree quickly. What sort of design decisions might you have to make?</li>
</ol>
<ul>
<li>A faster look up time will probably result from how the tree is structured</li>
<li>If tree is a BST, that can cut down on the lookup time by a half</li>
</ul>

