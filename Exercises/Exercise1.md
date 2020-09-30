<h1 id="exercise-2">Exercise 2</h1>
<ol>
<li>
<p>What are the differences between statically and dynamically typed langauges, what are the advantages of each?<br>
<strong>Statically Typed:</strong></p>
<ul>
<li>if the variable type is known at compile time
<ul>
<li>must specify what type each variable is</li>
</ul>
</li>
<li>some languages have a <em>type interface</em>
<ul>
<li>the ability to deduce the type of a variable on its own</li>
</ul>
</li>
<li>variables have some address in memory that will point to another address in memory (what the variable is assigned to)
<ul>
<li>when the variable is reassigned, the previous value’s memory is freed to avoid memory wastage</li>
</ul>
</li>
</ul>
<p><em>Advantage:</em> all kinds of checking can be done by the compiler, therfore a lot of trivial bugs can be caught earlier on</p>
<p><strong>Dynamically Typed:</strong></p>
<ul>
<li>the type is associated with run time values</li>
</ul>
<p><em>Advantage:</em> quicker writing</p>
</li>
<li>
<p>Java has 8 primitive data types. What are they, how are they used?</p>

<table>
<thead>
<tr>
<th>Type</th>
<th>What is it?</th>
<th>How is it used?</th>
</tr>
</thead>
<tbody>
<tr>
<td>boolean</td>
<td>Boolean value, either true or false</td>
<td>Used a lot in for loops, if statements etc. Whenever evaluating something to be yes or no</td>
</tr>
<tr>
<td>byte</td>
<td>Integer, 8 bits</td>
<td>From +127 to -128</td>
</tr>
<tr>
<td>char</td>
<td>Integer/single character</td>
<td>All unicode characters</td>
</tr>
<tr>
<td>short</td>
<td>Integer, 16 bits</td>
<td>From +32 767 to -32 768</td>
</tr>
<tr>
<td>int</td>
<td>Integer, 32 bits</td>
<td>From + 2 147 483 647 to - 2 147 483 648</td>
</tr>
<tr>
<td>long</td>
<td>Integer, 64 bits</td>
<td>From +9 223 372 036 854 775 807 to -9 223 372 036 854 775 808</td>
</tr>
<tr>
<td>float</td>
<td>Decimal, 32 bits</td>
<td>From 3.402,823,5 E+38 to 1.4 E-45</td>
</tr>
<tr>
<td>double</td>
<td>Decimal, 64 bits</td>
<td>From 1.797,693,134,862,315,7 E+308 to 4.9 E-324</td>
</tr>
</tbody>
</table></li>
<li>
<p>If a and b are instaniated boolean variables, what does the following evaluate to? Do you need more information? Why?</p>
<p><code>!((a || b) &amp;&amp; !(b || ! a || ! b))</code></p>
<pre><code>b || ! a || ! b == true - because of the b || !b
so...
  !((a || b) &amp;&amp; !true)
≡ !((a || b) &amp;&amp; false)
≡ !(false)
≡ true
</code></pre>
</li>
<li>
<p>Consider these variable declarations:</p>
<pre><code>int x = 2;
char c = 'a';
</code></pre>
<p>What do the following lines of Java evaluate to? Explain why. Hint: Look up the ACSII index table.<br>
a) x + c;<br>
<code>99</code> becuase a = 99 on ACSII</p>
<p>b) “” + c + x;</p>
<pre><code>ain
a2
</code></pre>
<p>c) x + c + “”;</p>
<pre><code>ain
99
</code></pre>
</li>
<li>
<p>a) Tinker around with some of the Java operations. Find something which suprised you. Does something behave differently from other languages you’ve used? Hopefully, some of you will be willing to share what you found with the class.</p>
<p>b) Do some indepdent research what are &amp; and | actually doing? Why does it functionally look equivalent to &amp;&amp; and ||?</p>
</li>
</ol>
<ul>
<li>&amp; and | evaluates both operations while &amp;&amp; || evaluate the second only if the first one is false</li>
</ul>
<ol start="6">
<li>
<p>NO IF STATEMENT CHALLANGE: Implement the following methods without using an if statement; only using material we have covered thus far.</p>
<p>a)</p>
<pre><code>	public static double myAbsoluteValue(double x){
		return Math.abs(x);
	}
</code></pre>
<p>b) You’re ordering pizzas for a party. In general, a child eats 2 slices of pizza, and adult eats 3, and a teenager eats 4. Pizzas have 8 slices total. Implement the function below which gives you the number of guests of each age group and returns the number of pizzas you should order. Bonus: find a solution without using the math library.</p>
<pre><code>	public static int pizzasToOrder(int child, int adult, int teen){
		...
	}
</code></pre>
</li>
</ol>

