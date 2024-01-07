---


---

<h2 id="install-mariadb">install mariaDB</h2>
<pre><code>sudo yum install mariadb-server mariadb
</code></pre>
<h4 id="change-root-password">change root password</h4>
<pre><code>mysql -u root -p -h localhost
</code></pre>
<h4 id="start-mariadb">start mariadb</h4>
<pre><code>sudo systemctl start mariadb
sudo mysql_secure_installation
</code></pre>
<h4 id="enable-mariadb">enable mariadb</h4>
<pre><code>sudo systemctl enable mariadb.service
</code></pre>
<h4 id="open-mariadb">open mariadb</h4>
<pre><code>mysql -u root -p
</code></pre>
<h4 id="mariadb-commands">mariadb commands</h4>
<pre><code>show databases;
create database testdb;
use testdb;
create table addrbook(name varchar(50) not null, phone char(10));
insert into addrbook(name, phone) values ("tom", "0912123456");insert into addrbook(name, phone) values ("mary", "0912123567");
select name,phone from addrbook;
update addrbook set phone="0987465123";
</code></pre>
<h2 id="php">PHP</h2>
<h4 id="install-php">install php</h4>
<pre><code>sudo yum install php php-mysql php-fpm
</code></pre>
<h4 id="restart-httpd-service">restart httpd service</h4>
<pre><code>sudo systemctl restart httpd.service
</code></pre>
<h4 id="section"></h4>
<pre><code>sudo vim /var/www/html/info.php
</code></pre>
<p>add this line into the info.php</p>
<blockquote>
&lt;?php phpinfo(); ?&gt;
</blockquote>
<p>test your website using browser, enter</p>
<pre><code>http://ip_address/info.php
</code></pre>
<h4 id="after-the-info.php-is-opened-remove-it-by-this">after the info.php is opened remove it by this</h4>
<pre><code>sudo rm -rf /var/www/html/info.php
sudo systemctl restart apache2
setsebool httpd_can_network_connect_db=1
</code></pre>
<h4 id="create-another-.php-file">create another .php file</h4>
<pre><code>&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Test PHP Connection Script&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;h3&gt;Welcome to the PHP Connect Test&lt;/h3&gt;

    &lt;?php	
    $dbname = 'testdb';
    $dbuser = 'root';
    $dbpass = 'centos';
    $dbhost = '127.0.0.1';
    $connect = mysql_connect($dbhost, $dbuser, $dbpass) or die("Unable to connect to '$dbhost'");
    mysql_select_db($dbname) or die("Could not open the database '$dbname'");
    $result = mysql_query("SELECT name,phone FROM addrbook");
    while ($row = mysql_fetch_array($result, MYSQL_NUM)) {
        printf("ID: %s  Name: %s &lt;br&gt;", $row[0], $row[1]);
    }
    ?&gt;
    
    &lt;/body&gt;
    &lt;/html&gt;
</code></pre>

