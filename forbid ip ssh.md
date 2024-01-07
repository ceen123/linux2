---


---

<h4 id="change-the-httpd.conf-file">change the httpd.conf file</h4>
<pre><code>nano /etc/httpd/conf/httpd.conf
</code></pre>
<h4 id="section"></h4>
<pre><code>&lt;Directory /var/www/html/b&gt;
        Order deny,allow
        Deny from 192.168.56.1 # the ip you want to forbbid
&lt;/Directory&gt;
</code></pre>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

