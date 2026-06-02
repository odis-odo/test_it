<br>

Encoding a file in base64 is as follows:

```cmd
certutil -encode infile outfile
```  

<br>

Decoding a file in base64 is as follows:

```cmd
certutil -decode encoded_file outfile
```  

<br>

The header and footer can be stripped with `findstr` with `-v`: 

```cmd
findstr /v CERTIFICATE  encoded_file.txt >removed-headers.txt
```  

<br>

To overwrite the file being decoded add the `-f` option:  

```cmd

certutil -decode -f encoded_file encoded_file_overwrite
```  

<br>

References  
[Windows base64 Encoding and Decoding Using certutil](https://dmfrsecurity.com/2017/01/07/windows-base64-encoding-and-decoding-using-certutil/)
