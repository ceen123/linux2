---


---

<h4 id="word-count">word count</h4>
<pre><code>cat -n test.txt
</code></pre>
<h4 id="how-to-use">how to use</h4>
<pre><code> wc [options] test.txt
</code></pre>
<p>options:</p>
<ul>
<li><code>-l</code>  – Prints the number of lines in a file.</li>
<li><code>-w</code>  – prints the number of words in a file.</li>
<li><code>-c</code>  – Displays the count of bytes in a file.</li>
<li><code>-m</code>  – prints the count of characters from a file.</li>
<li><code>-L</code>  – prints only the length of the longest line in a file.</li>
</ul>
<h4 id="tr-string-manipulation">‘tr’ string manipulation</h4>
<ul>
<li>
<p><code>-d</code> Deletes characters from the set1.</p>
</li>
<li>
<p><code>-s</code> Replaces repeated characters listed in the set with a single instance.</p>
</li>
<li>
<p><code>-c</code> Complements the set of characters in string1.</p>
</li>
<li>
<p><code>-C</code> Complements the set of characters in string1, handling multi-byte characters.</p>
</li>
<li>
<p><code>--complement</code> An alternative to  <code>-c</code>  and  <code>-C</code>  options.</p>
</li>
<li>
<p><code>-t</code> Truncates set1 to the length of set2.</p>
<pre><code> echo 'hello world' | tr -d 'world'
</code></pre>
</li>
</ul>
<blockquote>
<p>Output:<br>
'he ’</p>
</blockquote>

