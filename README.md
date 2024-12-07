# Ex.06 Book Front Cover Page Design
# Date:5/12/24
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
## (views.py):
~~~
from django.shortcuts import render,HttpResponse
def trail(request):
    return HttpResponse('<p>hello</p>')
def htm(request):
    return render(request,"home.html")
content = ''' 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>3D Cosmology Book Cover</title>
    
       

</head>
<body>
    <center>
        <div class="book-container">
            <div class="book-cover">
                <div class="front">
                    <h1 class="title">THE</h1>
                    <h1 class="title">ENCYCLOPEDIA</h1>
                    <h1 class="title">OF</h1>
                    <h1 class="title">COSMOLOGY</h1>
                    <h1 class="title">AUTHOR:</h1>
                    <p class="author">BY JHON DUO</p>
                    <img src="space.jpg" alt="Cosmology Image" class="cover-image">
                    <p class="description">EXPLORING THE UNIVERSE WITH MYSTRERIOUS WAY.</p>
                </div>
                <div class="back">
                    <p class="description">Cosmology studies how the history of the universe led to the stars, galaxies, and other features we can observe today. Cosmology is the study of the origin, development, structure, history, and future of the entire universe.</p>
                </div>
            </div>
        </div>
       
    </center>
</body>
<style>
    <style>
    body {
background-color: black;
color: yellow;
font-family: 'Arial', sans-serif;
margin: 0;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
}

.book-container {
perspective: 1000px;
}

.book-cover {
width: 500px;
height: 1000px;
background: black;
color: yellow;
border: 2px solid yellow;
text-align: center;
transition: transform 0.6s;
transform-style: preserve-3d;
}

.book-cover:hover {
transform: rotateY(180deg);
}

.front, .back {
position: absolute;
width: 100%;
height: 100%;
backface-visibility: hidden;
padding: 2em;
box-sizing: border-box;
}

.front {
background: black;
color: yellow;
}

.back {
background: black;
color: yellow;
transform: rotateY(180deg);
}

.title {
font-size: 3em;
margin: 0.2em 0;
}

.author {
font-size: 2em;
margin: 1em 0;
}

.cover-image {
width: 100%;
height: auto;
margin: 1em 0;
border: 2px solid yellow;
}

.description {
font-size: 1.5em;
margin: 1em 0;
}

button {
background-color: yellow;
color: black;
font-size: 1.2em;
border: none;
padding: 0.5em 1em;
cursor: pointer;
transition: background-color 0.3s;
}

button:hover {
background-color: darkorange;
}
</style>
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

#OUTPUT:
![Screenshot 2024-12-07 202515](https://github.com/user-attachments/assets/35cada16-2ec3-4530-8dbb-b541ea06299d)

 ![Screenshot 2024-12-07 202542](https://github.com/user-attachments/assets/9228dc20-fdf5-4ec0-a1b1-22f88b271b94)


# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
