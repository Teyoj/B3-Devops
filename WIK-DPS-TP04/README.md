# WIK-DPS-TP04

### Partie 1

```bash
hugoj@Teyoj:~/Documents/Ynov/B3/DevOps/B3-Devops/WIK-DPS-TP04$ curl -v localhost:8080/ping
*   Trying 127.0.0.1:8080...
* Connected to localhost (127.0.0.1) port 8080 (#0)
> GET /ping HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.81.0
> Accept: */*
> 
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Content-Type: application/json
< Date: Mon, 05 Dec 2022 11:38:01 GMT
< Connection: keep-alive
< Keep-Alive: timeout=5
< Transfer-Encoding: chunked
< 
* Connection #0 to host localhost left intact
{"host":"localhost:8080","user-agent":"curl/7.81.0","accept":"*/*"}
```