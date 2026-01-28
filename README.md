# Echoserver
Echo server and client using python socket
# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
</body>
</html>


class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('keerthi',2323)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
##  Architecture Diagram

```bash
+--------------------------+
|  User's Web Browser      |
|  (Client: Chrome/Firefox)|
+-----------+--------------+
            |
            |  HTTP Request (GET /)
            v
+-----------+--------------+
|   Python Web Server      |
| (http.server + Handler)  |
| - Listens on Port 8000   |
| - Handles GET Requests   |
| - Sends HTML Response    |
+-----------+--------------+
            |
            |  HTML Response
            v
+--------------------------+
|  User Sees Rendered Page |
|  <h1>Hello Web Server</h1>|
+--------------------------+
```


## OUTPUT:
### CLIENT OUTPUT:
### CODE :

<img width="709" height="482" alt="image" src="https://github.com/user-attachments/assets/7b81a3b2-1115-436c-9e72-1c507330d901" />


### OUTPUT :

<img width="617" height="239" alt="image" src="https://github.com/user-attachments/assets/85c945a6-6099-42c0-9ac5-55fe28440cda" />




### SERVER OUTPUT:
### CODE:

<img width="878" height="483" alt="image" src="https://github.com/user-attachments/assets/59309992-142e-4b69-96ab-e650322c4440" />


### OUTPUT :

<img width="652" height="219" alt="image" src="https://github.com/user-attachments/assets/479b1239-be8a-4b95-bb0a-8c36e7461b15" />


## RESULT:
The program is executed succesfully
