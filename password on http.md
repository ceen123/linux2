---


---

<h3 id="create-a-directory-in-html-folder">create a directory in html folder</h3>
<pre><code>cd /var/www/html
mkdir files
</code></pre>
<h4 id="create-user-and-password">create user and password</h4>
<pre><code>htpasswd -c .htpasswd user
</code></pre>
<h4 id="create-.htaccess">create .htaccess</h4>
<pre><code>nano .httaccess
</code></pre>
<h4 id="section"></h4>
<pre><code>AuthType Basic
AuthName "Private File Area"
AuthUserFile /var/www/html/files/.htpasswd
Require valid-user
</code></pre>
<h4 id="add-an-override-in-httpd.conf">add an override in httpd.conf</h4>
<pre><code>nano /etc/httpd/conf/httpd.conf
</code></pre>
<h4 id="section-1"></h4>
<pre><code>&lt;Directory /var/www/html/files&gt;
        Options Indexes
        AllowOverride AuthConfig
&lt;/Directory&gt;
</code></pre>
<h4 id="enter-your-ip-in-browers">enter your ip in browers</h4>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

