# Ex04 Places Around Me
# Date:10/10/2024
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
~~~
from django.shortcuts import render
from http.server import BaseHTTPRequestHandler, HTTPServer
from importlib.resources import contents
from django.http import HttpResponse

content='''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>image map</title>
</head>
<body>
    <img src="Screenshot 2024-12-07 112138.png" width="1500" alt="map image" usemap="#raganadan street">
    <map name="raganadan street">
        <area shape="rect" coords="1056,414,1290,531" href="T NAGAE/T.HTML" target="_blank" title="T NAGAR">
        <area shape="rect" coords="960,636,1209,721" href="GUINDY/G.HTML" target="_blank" title="GUINDY">
        <area shape="rect" coords="966,783,1142,864" href="NYARew folder/A.HTML" target="_blank" title="ADAYR">
        <area shape="rect" coords="1100,828,1319,921" href="KOVIL/K.HTML" target="_blank" title="VADA PALANI MURUGAN KOVIL">
        <area shape="rect" coords="641,524,900,778" href="SPET/S.HTML" target="_blank" title="SIDAPETA">
    </map>
</body>
</html>

'''
from http.server import HTTPServer,BaseHTTPRequestHandler
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address = ('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()
~~~
# OUTPUT
![Screenshot 2024-12-07 112138](https://github.com/user-attachments/assets/8ff9b344-fd57-4dda-a3ae-c0e69ad04a65)
![Screenshot 2024-12-07 110848](https://github.com/user-attachments/assets/f8bc7f61-c886-4607-9fba-e73c11840db5)

# RESULT
The program for implementing image maps using HTML is executed successfully.
