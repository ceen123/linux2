---


---

<h1 id="ssh-server">SSH Server</h1>
<h3 id="disable-firewalld">Disable firewalld</h3>
<pre><code>systemctl disable firewalld
</code></pre>
<h3 id="install-openssh-server-software-package">Install OpenSSH Server Software Package</h3>
<pre><code>sudo yum –y install openssh-server openssh-clients
</code></pre>
<h3 id="starting-ssh-service">Starting SSH Service</h3>
<pre><code>sudo systemctl start sshd
</code></pre>
<h3 id="check-sshd-status">Check sshd status</h3>
<pre><code>sudo systemctl status sshd
</code></pre>
<h3 id="enabledisable-openssh-service">Enable/Disable OpenSSH Service</h3>
<pre><code>sudo systemctl enable sshd
</code></pre>
<h3 id="section"></h3>
<pre><code>sudo systemctl disable sshd
</code></pre>
<h2 id="openssh-server-configuration">OpenSSH Server Configuration</h2>
<p>edit the file in this directory:</p>
<pre><code>sudo vim /etc/ssh/sshd_config
</code></pre>
<p>you can disable root login or changin port to increase security</p>
<blockquote>
<p>PermitRootLogin no<br>
Port 80</p>
</blockquote>
<pre><code>service sshd restart
</code></pre>
<h3 id="creating-rsa-key-pair">Creating RSA Key Pair</h3>
<pre><code>ssh-keygen
</code></pre>
<h3 id="copy-keygen">Copy keygen</h3>
<pre><code>ssh-copy-id username@remote_host
ssh-copy-id user1@192.168.123.123
</code></pre>
<h3 id="accessing-the-server-using-the-key-copied">Accessing the server using the key copied</h3>
<pre><code>ssh username@remote_host
ssh user1@192.168.123.123
</code></pre>
<h3 id="disabling-password-login">Disabling password login</h3>
<pre><code>sudo vi /etc/ssh/sshd_config
</code></pre>
<blockquote>
<p>PasswordAuthentication no</p>
</blockquote>
<pre><code>sudo systemctl restart sshd.service
</code></pre>

