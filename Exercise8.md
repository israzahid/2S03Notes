---


---

<h1 id="exercise-8">Exercise 8</h1>
<ol>
<li>Determine a better implementation for LinkedList so that appendBack is a lot simpler to implement (and efficient).</li>
</ol>
<ul>
<li>using tail variable instead of traversing entire list to add a value<pre><code>public void appendFront(int value) {
	Node node = new Node(value);
	if (isEmpty()) {
		tail = node;
	}
	node.next = head;
	head = node;
}

public void appendBack(int value) {
	Node node = new Node(value);
	if (isEmpty()){
		head = node;
		tail = node;
	}
	else {
		tail.next = node;
		tail = tail.next;
	}
}
</code></pre>
</li>
</ul>
<ol start="2">
<li>
<p>Implement the the getLength method in LinkedList. Come up with two different implementations of this. What are the advantages/disadvantages of each way?</p>
</li>
<li>
<p>Implement removeAll, insertAt, and contains in LinkedList</p>
<pre><code>public void contains (int value) {
	if (isEmpty()) {
		return false;
	}
	Node current = head;
	while (current.next != null) {
		if (current.value == value) {
			return true
		}
		current == current.next;
	}
	return false;
}

public void removeAll(int value) {
	if (isEmpty()) {
		return;
	}
	Node current = head;
	while (current.next != null) {
		if (current.next.value == value) {
			current.next = current.next.next;
		} 
		else {
			current = current.next;
		}
	}
	if (head.value == value) {
		head = head.next
	}
}
</code></pre>
</li>
<li>
<p>Implement reverse in LinkedList.</p>
<pre><code>public void reverse() {
	if (isEmpty() || head.next == null) {
		return;
	}
	Node current = head.next;
	Node prev = head;
	Node temp;
	while (current != null) {
		temp = current.next;
		current.next = prev;
		prev = current;
		current = temp;
	}
	temp = head;
	head = tail;
	tail = temp;
}
</code></pre>
</li>
<li>
<p>Think of some methods you wish were in DoublyLinkedList, implement some of them.</p>
</li>
<li>
<p>Create a merge method in DoublyLinkedList which takes in anouther DLL and returns a new DLL. Interleave the DLLs. For example, [8 &lt;–&gt; 9 &lt;–&gt; 1 &lt;–&gt; 2] and [10  &lt;–&gt; 7] should be merged to [8 &lt;–&gt; 10 &lt;–&gt; 9 &lt;–&gt; 7 &lt;–&gt; 1 &lt;–&gt; 2]</p>
</li>
</ol>

