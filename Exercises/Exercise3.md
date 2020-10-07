---


---

<h1 id="exercise-3">Exercise 3</h1>
<p>1<br>
a) Take a look online at all the Java String methods. Compare them to Python String methods. What luxuries/functionalities does Python have that you wish Java had?</p>
<p>b) Implement a method in Java to mimic the Python functionality you wish was present.</p>
<p>2<br>
a) Assume the method below is defined:</p>
<p>public static void f(int x) {<br>
int y = 2;<br>
if (x + y &gt; 5)<br>
y = x + y;<br>
System.out.println(y);<br>
System.out.println(y);<br>
}</p>
<p>What do you think is output when you call:</p>
<ul>
<li>f(4)</li>
<li>f(2)</li>
</ul>
<p>Now run it, does the output match with what you thought? What can you deduce about how Java runs this code/if statements in general?</p>
<p>b) Consider the if statement below. Simplify it as much as possible</p>
<p>if (x &gt; 100 &amp;&amp; y &gt; 0){<br>
if (y &gt; 100 &amp;&amp; x &gt; 0)<br>
return “A”;<br>
else if (y &gt; 100 || x &gt; 0)<br>
return “A”;<br>
else<br>
return “B”;<br>
}<br>
else if (y &lt;= 0 || x &lt;= 0){<br>
if (x == y)<br>
return “A”<br>
if (x &lt;= y &amp;&amp; x &gt;= y)<br>
return “B”;<br>
if (y &lt; x &amp;&amp; x &lt; y)<br>
return “C”;<br>
else<br>
return “A”;<br>
}<br>
else:<br>
if (100 &lt;= x || y &lt; 0)<br>
return “A”;<br>
if (x &lt;= 100 &amp;&amp; y &gt; 0)<br>
return “B”;<br>
else<br>
return “D”;</p>
<p>3<br>
Modify the while loop guessing game such that:<br>
a) The number does not change each time<br>
b) The program outputs whether the number is greater than or less than your guess</p>
<p>For each modification, if the player was playing intelligently, what is the best case and worst case number of times they will have to guess if the number is randomly generated between 1 and n?</p>
<p>4<br>
For or While? Can a for loop do something a while loop cannot? Can a while loop do something a for loop cannot? Give examples to prove your claims, or show the the general form one loop and be implemented as the general for of the other.</p>
<p>5<br>
Recall that chars in Java behave similarily to ints.</p>
<p>a) Using this information, implement a Caesar cipher encrpyt and decrypt method (you may need to “cast” certain terms as chars).</p>
<p>For information regarding a Caesat cipher see: <a href="https://en.wikipedia.org/wiki/Caesar_cipher">https://en.wikipedia.org/wiki/Caesar_cipher</a></p>
<p>b) When Julius was encrypting messages, he only had 26 characters to work with. You have more than that. What design decisions could you make to simplify the implementation and in someways make it harder to crack.</p>
<p>c) Assuming the messages are written in English text. How might you take an encrypted message and “guess” the key? Hint: think about which characters you see the most often. Note, I’m not expecting you to guess the key correctly 100% of the time. Try to implement this.</p>
<p>Start by writing a method which takes in a String and returns the char which appears the most in that String.</p>

