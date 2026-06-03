[curl Tutorial](https://curl.se/docs/tutorial.html)  

#### Download a webpage to file  

Get a webpage and store in a local file with a specific name:  


```
curl -o thatpage.html http://www.example.com/
```   

Get a webpage and store in local file with original name of document:  

```
curl -O http://www.example.com/index.html
```   

Fetch two files and store them with their remote names:   

```
curl -O www.haxx.se/index.html -O curl.se/download.html
```  

These also apply to downloading files as well.

<br>

#### Resuming File Transfers  

Continue downloading a document:  

```
curl -C - -o file ftp://ftp.example.com/path/file
```   

Continue uploading a document:   

```
curl -C - -T file ftp://ftp.example.com/path/file
```   

Continue downloading a document from a web server:  

```
curl -C - -o file http://www.example.com/
```

