---


---

<h2 id="install-nfs">install NFS</h2>
<h3 id="install-nfs-in-server">install nfs in server</h3>
<pre><code>sudo yum install nfs-utils
</code></pre>
<h3 id="section"></h3>
<pre><code>sudo systemctl enable rpcbind
sudo systemctl start rpcbind
</code></pre>
<h3 id="section-1"></h3>
<pre><code>sudo systemctl enable nfs
sudo systemctl start nfs
</code></pre>
<h3 id="in-the-server">in the server</h3>
<pre><code>mkdir /data -p
chmod 755 /data
</code></pre>
<h3 id="edit-the-data">edit the data</h3>
<pre><code>sudo vim /etc/exports
</code></pre>
<blockquote>
<p>/home/user/   192.168.56.106/24(rw,sync,no_root_squash,no_all_squash)</p>
</blockquote>
<pre><code>sudo systemctl restart nfs
showmount -e localhost
</code></pre>
<h3 id="then-install-nfs-and-enable-rpcbind-in-the-client">then install nfs and enable rpcbind in the client</h3>
<pre><code>sudo yum install nfs-utils
</code></pre>
<h4 id="section-2"></h4>
<pre><code>sudo systemctl enable rpcbind
sudo systemctl start rpcbind
</code></pre>
<h4 id="section-3"></h4>
<pre><code>showmount -e 192.168.56.106
</code></pre>
<h4 id="in-the-client">in the client</h4>
<pre><code>cd home/user
mkdir /nfs-data -p
</code></pre>
<h3 id="section-4"></h3>
<p>find your nfs directories and use this code</p>
<pre><code>$ sudo mount -t nfs 192.168.56.106:/data /nfs-data
</code></pre>
<p>rpm -qa | grep rpcbind</p>
<h4 id="in-then-client">in then client</h4>
<p>if not in nfs-data directory then:</p>
<pre><code>cd /nfs-data/
touch a
</code></pre>
<h4 id="in-the-server-1">in the server</h4>
<p>go to the data directory</p>
<pre><code>cd /data/
ls
</code></pre>
<p>this should show “a” file that is created from the client</p>

