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
<li>Implement the the getLength method in LinkedList. Come up with two different implementations of this. What are the advantages/disadvantages of each way?</li>
</ol>
<ul>
<li>First Method
<ul>
<li>modify a variable length as we add and remove elements</li>
<li>advantages: will not need to loop through the entire list to figure out the length, simply need to return length</li>
<li>disadvantages: with methods such as removeAll, will need to remove each time something is removed</li>
</ul>
</li>
<li>Second Method
<ul>
<li>loop through entire list and add until there is a null node</li>
<li>advantages: method explicitly for counting the list, less error prone</li>
<li>disadvantage: could add time complexity of n as we would need to traverse the entire list instead of just return a value</li>
</ul>
</li>
</ul>
<ol start="4">
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

public void insertAt (int value, int index) {
	Node newNode = new Node(value);
	if (isEmpty()) {
		head = newNode;
	} 
	else if (index == 0) {
		newNode.next = head;
		head = newNode;
	}
	else {
		Node current = head;
		Node previous = null;
		int i = 0;
		while (i != index) {
			previous = current;
			current = current.next;
			i++;
		}
		newNode.next = current;
		previous.next = newNode;
	}
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

