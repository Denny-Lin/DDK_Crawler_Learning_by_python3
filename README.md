# DDK_Crawler_Learning_by_python3
Use python3, requests, beautifulsoup4 and jupyter.

# Environment
1. OS: macOS Monterey Version 12.5
2. Browser: Google Chrome

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
Please refer to "References 5. 6.". </br>

# References
1. https://steam.oxxostudio.tw/category/python/spider/beautiful-soup.html
2. https://ithelp.ithome.com.tw/articles/10202121?sc=hot
3. https://blog.csdn.net/qq_22690765/article/details/78248606
4. https://blog.gtwang.org/programming/python-requests-module-tutorial/
5. https://www.cc.ntu.edu.tw/chinese/epaper/0044/20180320_4408.html
6. https://blog.toright.com/posts/1203/%E6%B7%BA%E8%AB%87-http-method%EF%BC%9A%E8%A1%A8%E5%96%AE%E4%B8%AD%E7%9A%84-get-%E8%88%87-post-%E6%9C%89%E4%BB%80%E9%BA%BC%E5%B7%AE%E5%88%A5%EF%BC%9F.html
