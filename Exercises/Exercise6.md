---


---

<h1 id="exercise-6">Exercise 6</h1>
<ol>
<li>
<p>Imagine you only had arrays available to you to store data. Could you implement myStack using arrays such that the height of myStack behaved dynamically. That is, the implementation has no “max height”? Hint: You can always create a new array if your current array reaches its length.</p>
<ol>
<li>create temp array</li>
<li>copy over the values from the original array to new array</li>
<li>values = temp (move pointer)</li>
</ol>
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
</li>
<li>
<p>Change the implementation of myQueue so we do not need to “shift” all the values forward. Hint: Think of the array as a circle, and keep track of the front and back indices.</p>
</li>
<li>
<p>Implement myQueue using two myStacks.</p>
</li>
</ol>

