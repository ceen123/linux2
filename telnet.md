---


---

<h2 id="insatll-telnet-service">insatll Telnet service</h2>
<h4 id="check-if-telnet-server-is-installed">check if telnet-server is installed</h4>
<pre><code>rpm-qa telnet-server 
rpm-qa xinetd
</code></pre>
<h4 id="if-not-then-install-using-this-code">if not then install using this code</h4>
<pre><code>yum-y install telnet-server 
yum-y install telnet 
yum-y install xinetd
</code></pre>
<h4 id="enable-xinetd">enable xinetd</h4>
<pre><code>systemctl enable xinetd.service 				
systemctl enable telnet.socket
</code></pre>
<h4 id="start-the-service">start the service</h4>
<pre><code>systemctl start telnet.socket 
systemctl start xinetd
</code></pre>
<h4 id="configure-firewall">configure firewall</h4>
<pre><code>firewall-cmd--permanent--add-port=23/tcp 　　
firewall-cmd--reload 　　
systemctl restart iptables 　　
systemctl disable firewalld 　　
systemctl stop firewalld
</code></pre>
<h4 id="to-enable-root-access-remotely-is-by-configuring-etcsecuretty">to enable root access remotely is by configuring /etc/securetty</h4>
<pre><code>nano /etc/securitty
</code></pre>
<p>add this on the end of the file and save</p>
<blockquote>
<p>pst/0<br>
pst/1</p>
</blockquote>

