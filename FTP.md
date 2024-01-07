---


---

<h3 id="install">install</h3>
<pre><code>sudo yum install vsftpd
</code></pre>
<h4 id="section"></h4>
<pre><code>sudo systemctl start vsftpd
sudo systemctl enable vsftpd
sudo systemctl status vsftpd
</code></pre>
<h4 id="section-1"></h4>
<pre><code>output
 vsftpd.service - Vsftpd ftp daemon
   Loaded: loaded (/usr/lib/systemd/system/vsftpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2018-11-22 09:42:37 UTC; 6s ago
 Main PID: 29612 (vsftpd)
   CGroup: /system.slice/vsftpd.service
           └─29612 /usr/sbin/vsftpd /etc/vsftpd/vsftpd.conf
</code></pre>
<h4 id="section-2"></h4>
<pre><code>sudo nano /etc/vsftpd/vsftpd.conf
</code></pre>
<h4 id="section-3"></h4>
<pre><code>anonymous_enable=YES
local_enable=YES
write_enable=YES
chroot_local_user=YES
</code></pre>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

