title: Find a file by extension
date: May 25th, 2020
slug: find-file-by-ext
category: Terminal

This comes in handy whenever I want to look for files that exists with a specific extension in a computer or server:

<pre>
<code class="bash">
find . -name "*.ext"
</code>
</pre>

In addition, sometimes, you might want to look for a bunch of files with a specific extension but with matching keywords:

<pre>
<code class="bash">
find .name "*.ext" | grep "keyword"
</code>
</pre>

## BONUS: Display list of files by extension with file sizes
Last month, I was trying to free up some space in our company server, so I realized that there were a lot of *.zip* files taking up a lot of space. So, I wrote a few commands to get me a list of zip files with their file sizes in sorting order into a .txt file:

<pre>
<code class="bash">
find . -iname \*.zip -exec du -sh {} \; &gt; zipfiles.txt
sort -rh zipfiles.txt > newfile.txt
</code>
</pre>

You can .zip with any extension to suit your needs! :)


