# EX01 Developing a Simple Webserver

# Date:22/09/2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from http.server import HTTPServer, BaseHTTPRequestHandler

content = '''
<!DOCTYPE html>
<html>
  <head>
    <title>Jegan (25017588)</title>
  </head>
  <body>
    <h1>Hello beginner!!</h1>
   <ul> <p>Jegan P(25017588)</p>
    <p>Welcome to my webserver</p>
    </ul>
    <img src="Screenshot (43).png" alt="Python Logo" width="200">
    <button>Click me!</button>
  </body>
</html>'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("Content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('', 8000)
httpd = HTTPServer(server_address, MyServer)
httpd.serve_forever()
```
# OUTPUT:
![alt text](</Screenshot (43).png>)
![alt text](<Screenshot (28).png>)
# RESULT:
The program for implementing simple webserver is executed successfully.

