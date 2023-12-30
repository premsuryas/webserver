# Developing a Simple Webserver

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
 <h2>4. String </h2>
 <h2>5. MERN Stack</h2>
 </body>
 </html>
 '''
class MyServer(BaseHTTPRequestHandler):
def do_GET(self):
print("Get request received...")
self.send_response(200)
self.send_header("content-type", "text/html")
self.end_headers()
self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
![serveroutput](serveroutput.png)
![serveroutput](clientoutput.png)
class MyServer(BaseHTTPRequestHandler):
def do_GET(self):
print("Get request received...")
self.send_response(200)
self.send_header("content-type", "text/html")
self.end_headers()
self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

## OUTPUT:
![output](![Screenshot 2023-12-30 134855](https://github.com/premsuryas/webserver/assets/147473858/57397b64-3d19-49d8-87be-d6978334d387)
)
## client output:
![output](![Screenshot 2023-12-30 135100](https://github.com/premsuryas/webserver/assets/147473858/cfae89a5-0f87-4ae6-943b-5eb6ef67356f)
)

## RESULT:
The program is executed succesfully
