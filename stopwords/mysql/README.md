Turkish-Stopwords For MySQL
===========================

<p>
    <a class="indexterm" name="idm47683249833216"></a>

    <a class="indexterm" name="idm47683249831728"></a>

    To override the default stopword list, set the
    <a class="link" href="server-system-variables.html#sysvar_ft_stopword_file"><code class="literal">ft_stopword_file</code></a> system
    variable. (See <a class="xref" href="server-system-variables.html" title="5.1.4&nbsp;Server System Variables">Section&nbsp;5.1.4, “Server System Variables”</a>.)
    The variable value should be the path name of the file
    containing the stopword list, or the empty string to disable
    stopword filtering. The server looks for the file in the
    data directory unless an absolute path name is given to
    specify a different directory. After changing the value of
    this variable or the contents of the stopword file, restart
    the server and rebuild your <code class="literal">FULLTEXT</code>
    indexes.
  </p><p>
    The stopword list is free-form. That is, you may use any
    nonalphanumeric character such as newline, space, or comma
    to separate stopwords. Exceptions are the underscore
    character (<span class="quote">“<span class="quote"><code class="literal">_</code></span>”</span>) and a single
    apostrophe (<span class="quote">“<span class="quote"><code class="literal">'</code></span>”</span>) which are
    treated as part of a word. The character set of the stopword
    list is the server's default character set; see
    <a class="xref" href="charset-server.html" title="10.1.3.1&nbsp;Server Character Set and Collation">Section&nbsp;10.1.3.1, “Server Character Set and Collation”</a>.
</p>

Also please read http://dev.mysql.com/doc/refman/5.0/en/fulltext-stopwords.html for MySQL Fulltext stop words.