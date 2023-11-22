## EX01 Developing a Simple Webserver

## AIM:
To develop a simple webserver to serve html pages.

### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Languages</h1>
<h2>1.HTML</h2>
<h2>2. CSS</h2>
<h2>3. JavaScript</h2>
<h2>4. ASP.NET </h2>
<h2>5. XML </h2>
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
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()

### Output:
![Screenshot from 2023-11-22 18-52-36](https://github.com/DivyaMunirathnamm/simplewebserver/assets/147474097/1f52f5e6-a5c1-4c4c-8516-5065dfa899ae)


## RESULT:
The program for implementing simple webserver is executed successfully.
