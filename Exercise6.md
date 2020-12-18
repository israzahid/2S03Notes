---


---

<h1 id="exercise-6">Exercise 6</h1>
<ol>
<li>
<p>Imagine you only had arrays available to you to store data. Could you implement myStack using arrays such that the height of myStack behaved dynamically. That is, the implementation has no “max height”? Hint: You can always create a new array if your current array reaches its length.</p>
<ol>
<li>create temp array with a new size</li>
<li>copy over the values from the original array to new array</li>
<li>values = temp (move pointer)</li>
</ol>
<pre><code>public class myStack() {
    private int[] values;
    private int DEFAULT_SIZE = 5;
    public int height;

	public myStack() {
		this.values = new int[DEFAULT_SIZE];
		this.height = 0;
	}

	public void push(int n) {
		if (height == values.length){
			resizeUp;
		}
		values[height] = n;
		height++;
	}

	public int pop() {
		int top = values[height-1]
		if (height &lt; values.length/2 &amp;&amp; height &gt; DEFAULT_SIZE) {
			resizeDown();
		}
		height--;
		return top;
	}

	public boolean isEmpty() {
		return height == 0;
	}

	public int getHeight() {
		return height;
	}

	public int peek() {
		return values[height-1];
	}
	private void resizeUp() {
		int[] temp = new int[2*values.length];
		for (int i = 0; i &lt; height; i++) {
			temp[i] = values[i];
		}
		values = temp;
	}
	private void resizeDown() {
		int[] temp = new int[(3/4)*values.length];
		for (int i = 0; i &lt; height; i++) {
			temp[i] = values[i];
		}
		values = temp;
	}
}
</code></pre>
</li>
<li>
<p>Write a method which takes in a String of parentheses and returns true iff they are “balanced”. For example the following Strings should return true:<br>
“(((())))”<br>
“()()()(())(()())”<br>
“()()((()))”<br>
and the following Strings should return false:<br>
“(()”<br>
“)()()”<br>
“((((())))))))((()”<br>
Hint: Use a stack.<br>
Imagine now your String could contain other characters as well for example they could be of the form: “k(y(x+1) + z(x-1))(z+y)^2”, does your implementation change all that much? What if you need to check if multiple types of parentheses/brackets were balanced? For example: “{(){[]}}” is balanced, while “{}([)]” is not.</p>
<pre><code>public class BalancedBrackets {
	myStack&lt;Character&gt; stack = new myStack&lt;Character&gt;();
	public boolean isBalanced(String exp) {
		boolean balanced = true;
		for (int i = 0; i &lt; exp.length(); i++) {
			char symbol = exp.charAt(i);
			if (symbol == '(') {
				stack.push(symbol);
			}
			else {
				if (stack.isEmpty()) {
					balanced = false;
				}
				else {
					stack.pop();
				}
			}
		}
	if (balanced &amp;&amp; stack.isEmpty()) {
		return true;
	}
	return false;
  }
}
</code></pre>
</li>
<li>
<p>Change the implementation of myQueue so we do not need to “shift” all the values forward. Hint: Think of the array as a circle, and keep track of the front and back indices.</p>
<pre><code>public class myQueue {
	private int[] values;
	private int length;
	private int front = 0;
	private int back = 0;
	
	public myQueue() {
		values = new int[10];
		length = 0;
	}

	public void add (int value) {
		values[back] = value;
		length++;
		if (back = values.length - 1) {
			back = 0;
		}
		else {
			back++;
		}
	}

	public int remove() {
		int value = values[front];
		if (front == values.length - 1) {
			front = 0;
		}
		else {
			front++;
		}
		return value;
	}

	public int peak() {
		return values[front];
	}

	public boolean isEmpty() {
		return length == 0;
	}
}
</code></pre>
</li>
<li>
<p>Implement myQueue using two myStacks.</p>
<pre><code>public class myQueue {  
    myStack s1 = new myStack();  
  myStack s2 = new myStack();  
  
 public void add (int value) {  
        s2.push(value);  
  }  
  
    public int remove() {  
        if (s1.isEmpty()){  
            while (!s2.isEmpty()) {  
                s1.push(s2.pop());  
  }  
        }  
        return s1.pop();  
  }  
}
</code></pre>
</li>
</ol>

