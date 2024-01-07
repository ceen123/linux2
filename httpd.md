---


---

<h1 id="install-httpd">Install httpd</h1>
<blockquote>
<p>use super user 2.getenforce-&gt;Disabled  3. systemctl status firewalld —&gt;inactive</p>
</blockquote>
<pre><code>getenforece 0
</code></pre>
<h3 id="section"></h3>
<pre><code>yum install httpd -y
</code></pre>
<h3 id="check-whether-the-apache-http-server-httpd-is-installed-on-a-system">Check whether the Apache HTTP Server (httpd) is installed on a system</h3>
<pre><code>rpm -qa | grep httpd
</code></pre>
<h3 id="create-a-.html-file-and-place-in-directory">Create a .html file and place in directory</h3>
<pre><code>cd /var/www/html
echo "hello world, Tom" &gt;&gt; hi.html
</code></pre>

