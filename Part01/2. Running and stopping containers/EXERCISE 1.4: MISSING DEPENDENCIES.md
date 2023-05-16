### Start the container with the given process:
 ```console
 docker run -d -it --name search ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
 ```
 
 ### In a new separate terminal enter the container:
  ```console
 docker exec -it search bash
 ```
 
 ### Installing the missing dependencies 
 ```console
 apt-get update
 apt-get install -y curl
 ```
 
 ### Inside the container try "curl helsinki.fi"
  ```console
root@3f4c7a91864d:/# curl helsinki.fi
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.20.1</center>
</body>
</html>
 ```
