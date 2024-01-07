---


---

<h3 id="disable-selinux">disable selinux</h3>
<pre><code>get enforced
</code></pre>
<h3 id="section"></h3>
<pre><code>vim /etc/selinux/config
</code></pre>
<blockquote>
<p>SELINUX=disabled</p>
</blockquote>
<h3 id="section-1"></h3>
<pre><code>systemctl status firewalld
</code></pre>
<p>make sure the firewalld us inactive (dead)</p>
<h3 id="install-samba">install samba</h3>
<pre><code>yum install samba samba-client samba-common -y
</code></pre>
<h4 id="create-samba-directory">create samba directory</h4>
<pre><code>mkdir /test_samba -p
</code></pre>
<h3 id="section-2"></h3>
<pre><code>chown nobody /test_samba
</code></pre>
<h3 id="section-3"></h3>
<pre><code>ls -l -d /test_samba/
</code></pre>
<h3 id="section-4"></h3>
<pre><code>chmod 777 /test_samba/
</code></pre>
<h3 id="change-samba-smb.conf">change samba smb.conf</h3>
<pre><code>vim /etc/samba/smb.conf
</code></pre>
<p>insert in the smb.conf</p>
<pre><code>[test]
    comment = share /test_samba directory to windows
    path = /test_samba
    read only = no
    guest ok = yes
    browsable = yes
</code></pre>
<h3 id="section-5"></h3>
<pre><code>systemctl restart smb
systemctl status smb
</code></pre>
<h3 id="to-change-your-smb-password">to change your smb password</h3>
<pre><code>smbpasswd -a user
</code></pre>
<h3 id="then-enter-ipaddr-in-your-windows-file-explorer">then enter \‘ipAddr’ in your windows file explorer</h3>

