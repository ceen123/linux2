---


---

<h2 id="install-ngrok">install ngrok</h2>
<h3 id="login-httpsngrok.com">Login <a href="https://ngrok.com/">https://ngrok.com</a></h3>
<p>download ngrok .zip file</p>
<pre><code>wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz
</code></pre>
<p>unzip</p>
<pre><code>tar zxvf ngrok-v3-stable-linux-amd64.tgz
</code></pre>
<p>get authentication token</p>
<blockquote>
<p><a href="https://dashboard.ngrok.com/get-started/your-authtoken">https://dashboard.ngrok.com/get-started/your-authtoken</a></p>
</blockquote>
<h4 id="start-ngrok">start ngrok</h4>
<pre><code>./ngrok config add-authtoken 	2VvPdP6jut9Ea7abeZTazB1CjB6_3fPtDJEijTUdAmETeSCvy
</code></pre>
<h3 id="section"></h3>
<pre><code>ngrok http 80
</code></pre>

