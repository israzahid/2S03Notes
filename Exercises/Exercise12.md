---


---

<h1 id="exercise-12">Exercise 12</h1>
<ol>
<li>Take a look at the incorrect solution in BST2.java. Work out why this solution does not behave as you may expect.</li>
</ol>
<ul>
<li>This functionality does not work because we are changing the hookups, which should be our main focus</li>
</ul>
<ol start="2">
<li>
<p>In the same file, at the end, there is a solution which has been commented out. As saw in lecture, this solution works, unless you delete the root node. Understand why this solution fixes the issues or erroneous one. Also, modify the code so we can now delete the root.</p>
</li>
<li>
<p>This code is long and messy and hard to understand at points! Can you think of a better way to implement the BST so we have the simplicity fo the incorrect solution but it also works! Remember, you can change the implementation of Node.java as well. Hint: When looking at Linked Lists we say a “doubly” Linked List. What would that look like in a Binary Tree?</p>
</li>
</ol>
<p>DoubleNode.java</p>
<pre><code>public class DoubleNode {  
  
    public int value;  
	 public DoubleNode left;  
	 public DoubleNode right;  
	 public DoubleNode parent;  
  
	 public DoubleNode(int value) {  this.value = value;  }  
  
	 public boolean hasLeftChild() {  return left != null;  }  
  
	 public boolean hasRightChild() {  return right != null;   }  
 
     public boolean isLeaf() {  return left == null &amp;&amp; right == null;  }  
    
     public boolean isLeftChild() {  return value &lt; parent.value;  }
    
     public boolean isRightChild() {  return value &gt; parent.value;  }   
}
</code></pre>
<p>Delete Method</p>
<pre><code>public void delete(int value) {  
   if(root == null) {  
      return;  
  }  
   deleteRec(root, value);  
}  
  
private void deleteRec(DoubleNode node, int value) {  
   if(node == null) {  
      return;  
  }  
     
   if(node.value == value) {  
      deleteNode(node);  
  }  
   else if(value &lt; node.value) {  
      deleteRec(node.left, value);  
  }  
   else if(value &gt; node.value){  
      deleteRec(node.right, value);  
  }  
     
}  
  
private void deleteNode(DoubleNode node) {  
   if(node.isLeaf()) {  
      if(node.isLeftChild()) {  
         node.parent.left = null;  
	  }  
      else {  
         node.parent.right = null;  
	  }  
   }  
   else if(!node.hasLeftChild()) {  
      if(node.isLeftChild()) {  
         node.parent.left = node.right;  
	  }	  
      else {  
         node.parent.right = node.right;  
	  }  
      node.right.parent = node.parent;  
  }  
   else if(!node.hasRightChild()) {  
      if(node.isLeftChild()) {  
         node.parent.left = node.left;  
	  }  
      else {  
         node.parent.right = node.left;  
	  }  
      node.left.parent = node.parent;  
  }  
   else {  
      int k = getMinRec(node.right);  
	  node.value = k;  
	  deleteRec(node.right, k);  
  }
}  
</code></pre>

