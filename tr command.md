---


---

<h4 id="replace-character">replace character</h4>
<pre><code>$ echo 'Linux' | tr 'nux' 'one'
</code></pre>
<blockquote>
<p>Lione</p>
</blockquote>
<h4 id="replace-character-range">replace character range</h4>
<pre><code>$ echo 'among' | tr 'a-f' 'x-z'
</code></pre>
<blockquote>
<p>xmong</p>
</blockquote>
<h4 id="ignore-specific-characters">Ignore Specific Characters</h4>
<pre><code>$ echo 'linux' | tr -c 'l' 'y' 
</code></pre>
<blockquote>
<p>lyyyyy</p>
</blockquote>
<h4 id="delete-specific-characters">Delete Specific Characters</h4>
<pre><code>$ echo 'Ubuntu' | tr -d 'Ub'
</code></pre>
<blockquote>
<p>untu</p>
</blockquote>
<h4 id="remove-extra-spaces">Remove Extra Spaces</h4>
<pre><code>$ echo 'Linux   \   Ubuntu' | tr -s '  '
</code></pre>
<blockquote>
<p>Linux \ Ubuntu</p>
</blockquote>
<h4 id="change-lowercase-to-uppercase">Change LowerCase to UpperCase</h4>
<pre><code>$ echo "linux is the best command prompt. " | tr "a-z" "A-Z"
</code></pre>
<blockquote>
<p>LINUX IS THE BSET COMMAND PROMPT.</p>
</blockquote>
<h4 id="remove-non-numeric-characters">Remove Non-Numeric Characters</h4>
<pre><code>$ echo ‘your pin is 200382’ | tr -cd ‘[:digit:]’
</code></pre>
<blockquote>
<p>200382</p>
</blockquote>
<h4 id="remove-numeric-characters">Remove Numeric Characters</h4>
<pre><code>$ echo ‘your pin is 200382’ | tr -d [:digit:]
</code></pre>
<blockquote>
<p>your pin is</p>
</blockquote>
<h4 id="use-the-tr-command-with-bash-scripts">Use the tr Command With Bash Scripts</h4>
<pre><code>$ tr -cd [:print:]&lt; hello.sh
</code></pre>
<blockquote>
<p>HELLO<br>
$ cat <a href="http://hello.sh">hello.sh</a> | tr -d E<br>
HLLO</p>
</blockquote>

