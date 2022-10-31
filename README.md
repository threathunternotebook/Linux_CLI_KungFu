# Linux_CLI_KungFu
Helpful Linux command line tips

## Passwords with special characters
Use a username with a password containing special characters. Add 3 single quotes before and 3 single quotes after. This will escape the special characters (in this case, !!) and allow the full password to be passed to the application (in this case, Elasticsearch).
<pre><code>curl --insecure -u threathunter@hunt.com:'''MyPasswordwithSpecialCharacters!!''' -XGET https://127.0.0.1:9200/so-zeek-2021.07.01/_search?pretty</code></pre>

## Removing newline characters from a file using sed
In this case we are trying to join two seperate lines into one. We need to remove the newline from one line in order to achieve this.
<pre><code>sed ':a;N;$!ba;s/\n//g' input.file > output.file</code></pre>
