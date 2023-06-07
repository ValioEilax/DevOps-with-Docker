## Changes to the docker-compose.yml
Removed the unnecessary ports 5000 and 8080 from backend and frontend. 

## Port scan report
```console
$ docker run -it --rm --network host networkstatic/nmap localhost
Starting Nmap 7.92 ( https://nmap.org ) at 2023-06-07 20:14 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0000040s latency).
Not shown: 995 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
111/tcp  open  rpcbind
631/tcp  open  ipp
8084/tcp open  websnp

Nmap done: 1 IP address (1 host up) scanned in 0.13 seconds
```
