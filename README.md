# HostJavascriptFiles

To host JS files and have the correct MIME type returned. When hosting a self hosted server for files. 
ie: 
```bash
php -s 127.0.0.1
```

Add another file 'index.php' with the contents

```bash
<?php
header("Content-Type: text/javascript");
?>
```

This will set the correct mime type for Javascript
Curl to the self hosted sites returns
```
* Connected to 127.0.0.1 (127.0.0.1) port 80 (#0)
> GET / HTTP/1.1
> Host: 127.0.0.1
> User-Agent: curl/7.74.0
> Accept: */*
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Host: 127.0.0.1
< Date: Thu, 20 May 2021 22:35:48 GMT
< Connection: close
< X-Powered-By: PHP/7.4.15
< Content-type: text/javascript;charset=UTF-8
```
