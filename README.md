# DDK_Crawler_Learning_by_python3
Use python3, requests, beautifulsoup4 and jupyter.

# Environment
OS: macOS Monterey Version 12.5

# Install modules
Mac has Python 3.8.9 by default. </br>

```sh
python3 --version
python3 -m pip install beautifulsoup4 requests jupyter --user
```

# Run jupyter
```sh
/Users/YOUR_USER_NAME/Library/Python/3.8/bin/jupyter notebook
```
# HTTP interactions
We play the role of the client, so we should interact with the server. </br>

## How to get?
```python3
import requests
x = requests.get(url, parameter)
print(x.text)
```
```python3
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM) #IPV4, TCP
s.connect(ip, port)
s.send(b"GET / HTTP/1.1 \r\n")
data = s.recv(buffer)
print(data)
```
## How to post?
```python3
import requests
x = requests.post(url, parameter)
print(x.text)
```
```python3
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM) #IPV4, TCP
s.connect(ip, port)
s.send(b"POST /xxx HTTP/1.1\r\n")
data = s.recv(buffer)
print(data)
```
## When to choose get or post?
Please refer to "References 5". </br>

# References
1. https://steam.oxxostudio.tw/category/python/spider/beautiful-soup.html
2. https://ithelp.ithome.com.tw/articles/10202121?sc=hot
3. https://blog.csdn.net/qq_22690765/article/details/78248606
4. https://blog.gtwang.org/programming/python-requests-module-tutorial/
5. https://www.cc.ntu.edu.tw/chinese/epaper/0044/20180320_4408.html
