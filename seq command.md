---


---

<h4 id="basic-sequencing">basic sequencing</h4>
<pre><code>$ seq 5
1
2
3
4
5
</code></pre>
<h4 id="sequnce-from-1-1000">sequnce from 1-1000</h4>
<pre><code>$ time seq 1000 | tail -8
993
994
995
996
997
998
999
1000

real    0m0.003s
user    0m0.001s
sys     0m0.003s
</code></pre>
<h4 id="sequence-with-every-times-4">sequence with every times 4</h4>
<pre><code>$ seq 2024 4 2055
2024
2028
2032
2036
2040
2044
2048
2052
</code></pre>
<h4 id="decending-sequencing-by--10-every-seq">decending sequencing by -10 every seq</h4>
<pre><code>$ seq 100 -10 0
100
90
80
70
60
50
40
30
20
10
0
</code></pre>
<h4 id="use-a-bash-loop-every-seq">use a bash loop every seq</h4>
<pre><code>$ for yr in `seq 2024 4 2055`
&gt; do
&gt;     echo "$yr is a leap year"
&gt; done
2024 is a leap year
2028 is a leap year
2032 is a leap year
2036 is a leap year
2040 is a leap year
2044 is a leap year
2048 is a leap year
2052 is a leap year
</code></pre>
<h4 id="change-all-the-sequence-number-of-digit-to-the-largest-number-in-the-list">change all the sequence number of digit to the largest number in the list</h4>
<pre><code>$ seq -w 1 11 100
001
012
023
034
045
056
067
078
089
100
</code></pre>
<h4 id="specifically-adding-how-many-digit-into-the-sequence">Specifically adding how many digit into the sequence</h4>
<p>$ seq -f “%03g” 10<br>
001<br>
002<br>
003<br>
004<br>
005<br>
006<br>
007<br>
008<br>
009<br>
010</p>
<h4 id="uses-decimal-point-to-sequencing-and-uses-column-to-create-a-table-column">uses decimal point to sequencing, and uses column to create a table column</h4>
<pre><code>$ seq 0.3 0.3 9.9 | column
0.3     1.5     2.7     3.9     5.1     6.3     7.5     8.7     9.9
0.6     1.8     3.0     4.2     5.4     6.6     7.8     9.0
0.9     2.1     3.3     4.5     5.7     6.9     8.1     9.3
1.2     2.4     3.6     4.8     6.0     7.2     8.4     9.6
</code></pre>
<h4 id="created-space-for-each-sequence-instead-of-going-down-the-collumn">created space for each sequence instead of going down the collumn</h4>
<pre><code>$ seq -s "  " 0.3 0.3 9.9
0.3  0.6  0.9  1.2  1.5  1.8  2.1  2.4  2.7  3.0  3.3  3.6  3.9  4.2  4.5  4.8  5.1  5.4  5.7  6.0  6.3  6.6  6.9  7.2  7.5  7.8  8.1  8.4  8.7  9.0  9.3  9.6  9.9
</code></pre>
<h4 id="separating-the-sequence-by-using----and---">separating the sequence by using ’ : ’ and ’ , ’</h4>
<pre><code>$ seq -s: 2024 4 2050
2024:2028:2032:2036:2040:2044:2048
</code></pre>
<h4 id="section"></h4>
<pre><code>$ seq -s, 100 -10 0
100,90,80,70,60,50,40,30,20,10,0
</code></pre>
<h4 id="multiplication">multiplication</h4>
<pre><code>$ seq -s* 1 10 | bc
3628800

$ seq -s + 1 10 | bc
55

$ seq -s "`echo -e "t"`" 5 11
5       6       7       8       9       10      11
</code></pre>

