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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guindy, Chennai</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        header {
            background-color: #004d99;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }
        section {
            padding: 20px;
            max-width: 800px;
            margin: 20px auto;
            background: white;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
        }
        h1, h2 {
            color: #004d99;
        }
        p {
            margin: 10px 0;
            color: #333;
        }
        a {
            color: #004d99;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Guindy, Chennai</h1>
    </header>
    <section>
        <h2>About Guindy</h2>
        <p>
            Guindy is a prominent neighborhood in Chennai, known for its vibrant blend of commercial, residential, and ecological zones.
            It is home to the famous Guindy National Park, one of the few national parks located within a city, offering lush greenery and a 
            sanctuary for various flora and fauna.
        </p>
        <p>
            The area is also an important business hub with the Guindy Industrial Estate, housing several IT and manufacturing companies. 
            Its strategic location near Chennai International Airport and major roadways makes it a key transit point.
        </p>
        <p>
            For nature enthusiasts and urban explorers alike, Guindy offers a unique balance of city life and natural beauty.
            Learn more about its attractions on the <a href="https://www.tn.gov.in/" target="_blank">official Tamil Nadu website</a>.
        </p>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vadapalani Murugan Temple</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background-color: #f9f4e9;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #4b3832;
        }
        header {
            background-color: #a52a2a;
            color: white;
            text-align: center;
            padding: 15px;
        }
        header h1 {
            margin: 0;
        }
        section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
        }
        h2 {
            color: #a52a2a;
        }
        p {
            margin: 10px 0;
        }
        a {
            color: #a52a2a;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Vadapalani Murugan Temple</h1>
    </header>
    <section>
        <h2>About Vadapalani Murugan Temple</h2>
        <p>
            The Vadapalani Murugan Temple, located in Chennai, Tamil Nadu, is a revered shrine dedicated to Lord Murugan. 
            It is one of the most popular temples in the city and attracts thousands of devotees daily, especially during 
            festivals like Thaipusam and Panguni Uthiram.
        </p>
        <p>
            The temple, known for its stunning Dravidian architecture, features intricate carvings and a majestic Rajagopuram (entrance tower). 
            It is believed that the deity here has miraculous powers, and the temple is particularly famous for blessings related to marriage and childbearing.
        </p>
        <p>
            With its serene atmosphere and rich cultural heritage, Vadapalani Murugan Temple stands as a spiritual landmark in Chennai. 
            For more information, visit the <a href="https://www.tnhrce.org/" target="_blank">official Tamil Nadu HRCE website</a>.
        </p>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adyar, Chennai</title>
    <style>
        body {
            font-family: 'Verdana', sans-serif;
            background-color: #eaf7f9;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #34495e;
        }
        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 15px;
        }
        header h1 {
            margin: 0;
        }
        section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
        }
        h2 {
            color: #2c3e50;
        }
        p {
            margin: 10px 0;
        }
        a {
            color: #2c3e50;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Adyar, Chennai</h1>
    </header>
    <section>
        <h2>About Adyar</h2>
        <p>
            Adyar is one of the most prominent neighborhoods in Chennai, Tamil Nadu. Situated along the banks of the Adyar River, 
            this area is known for its serene environment and historical significance. Adyar is home to the famous Theosophical Society, 
            which serves as a global hub for spiritual and philosophical learning.
        </p>
        <p>
            The area also boasts lush greenery and recreational spaces such as the Adyar Eco Park and the Broken Bridge, a popular 
            spot for photography and birdwatching. Additionally, Adyar is known for its vibrant residential community and well-developed 
            infrastructure, making it a desirable locality in Chennai.
        </p>
        <p>
            Whether it's the peaceful riverside or the bustling city life, Adyar offers a unique blend of tradition and modernity. 
            Learn more about the attractions in Adyar on the <a href="https://www.chennaicorporation.gov.in/" target="_blank">Chennai Corporation website</a>.
        </p>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saidapet, Chennai</title>
    <style>
        body {
            font-family: 'Tahoma', sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #333333;
        }
        header {
            background-color: #006400;
            color: white;
            text-align: center;
            padding: 15px;
        }
        header h1 {
            margin: 0;
        }
        section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
        }
        h2 {
            color: #006400;
        }
        p {
            margin: 10px 0;
        }
        a {
            color: #006400;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Saidapet, Chennai</h1>
    </header>
    <section>
        <h2>About Saidapet</h2>
        <p>
            Saidapet, located in Chennai, Tamil Nadu, is a bustling neighborhood with historical and cultural importance. 
            It serves as a major transit hub, connecting various parts of the city through road and rail networks.
        </p>
        <p>
            One of the key landmarks in Saidapet is the <strong>Saidapet Court</strong>, which is one of the oldest in Chennai. 
            The neighborhood is also known for the <strong>Sri Prasanna Venkatesa Perumal Temple</strong>, a significant religious site 
            that attracts devotees from all over the city.
        </p>
        <p>
            With its mix of commercial establishments, residential areas, and cultural heritage, Saidapet offers a unique slice of Chennai's 
            vibrant lifestyle. Learn more about Saidapet on the <a href="https://www.chennaicorporation.gov.in/" target="_blank">Chennai Corporation website</a>.
        </p>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>T. Nagar, Chennai</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #2c3e50;
        }
        header {
            background-color: #8b0000;
            color: white;
            text-align: center;
            padding: 15px;
        }
        header h1 {
            margin: 0;
        }
        section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
        }
        h2 {
            color: #8b0000;
        }
        p {
            margin: 10px 0;
        }
        a {
            color: #8b0000;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to T. Nagar, Chennai</h1>
    </header>
    <section>
        <h2>About T. Nagar</h2>
        <p>
            Thyagaraya Nagar, popularly known as T. Nagar, is one of the most vibrant and bustling neighborhoods in Chennai. 
            Renowned as a shopping hub, it is the go-to destination for gold jewelry, silk sarees, and other traditional items, 
            attracting both locals and tourists.
        </p>
        <p>
            The area is also home to several parks, including the well-known Panagal Park, which provides a green retreat amidst 
            the busy streets. T. Nagar is a hub for cultural activities, with many theaters and venues hosting events and performances.
        </p>
        <p>
            Its combination of commercial, residential, and cultural significance makes T. Nagar a dynamic part of Chennai. 
            For more details, visit the <a href="https://www.chennaicorporation.gov.in/" target="_blank">Chennai Corporation website</a>.
        </p>
    </section>
</body>
</html>
~~~
# OUTPUT
![Screenshot 2024-12-07 112138](https://github.com/user-attachments/assets/8ff9b344-fd57-4dda-a3ae-c0e69ad04a65)
![Screenshot 2024-12-07 110848](https://github.com/user-attachments/assets/f8bc7f61-c886-4607-9fba-e73c11840db5)

# RESULT
The program for implementing image maps using HTML is executed successfully.
