# tech_task
<pre>
psavelkov@testvm:~$ history 100
    1  ip a
    2  sudo apt-get update
    3  sudo apt-get install     apt-transport-https     ca-certificates     curl     gnupg     lsb-release
    4  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    5  echo   "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
    6    $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    7  sudo apt-get update
    8  sudo apt-get install docker-ce docker-ce-cli containerd.io
    9  systemctl list-unit-files --state=enabled | grep docker
   10  systemctl status docker
   11  sudo usermod -aG docker $USER
   12  exit
   13  nano index.html
   14  docker run --name nginx-techtask -p 80:80 -v ~/index.html:/usr/share/nginx/html/index.html:ro -d nginx
   15  history 100
psavelkov@testvm:~$ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                               NAMES
12f51c3db803   nginx     "/docker-entrypoint.…"   33 seconds ago   Up 31 seconds   0.0.0.0:80->80/tcp, :::80->80/tcp   nginx-techtask
psavelkov@testvm:~$ curl -v -XGET http://localhost
Note: Unnecessary use of -X or --request, GET is already inferred.
*   Trying 127.0.0.1:80...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 80 (#0)
> GET / HTTP/1.1
> Host: localhost
> User-Agent: curl/7.68.0
> Accept: */*
>
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx/1.21.0
< Date: Mon, 28 Jun 2021 18:49:29 GMT
< Content-Type: text/html
< Content-Length: 148
< Last-Modified: Mon, 28 Jun 2021 18:41:38 GMT
< Connection: keep-alive
< ETag: "60da17e2-94"
< Accept-Ranges: bytes
<
&lt;!doctype html>
&lt;html lang="en">
&lt;head>
  &lt;meta charset="UTF-8">
  &lt;title>Hello World!&lt;/title>
&lt;/head>
&lt;body>
&lt;h1>Hello World!&lt;/h1>
&lt;/body>
&lt;/html>
* Connection #0 to host localhost left intact
psavelkov@testvm:~$
</pre>
