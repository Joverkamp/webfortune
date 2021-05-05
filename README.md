# webfortune
This program allows users to communicate to a linux command line via webserver to receive fortunes, use cowsay, and a combination of both.

# Building
To build this application you must have docker installed. Then to create your docker image, run this command `docker build -t <repository> .` where `<repository>` is how you want to identify your docker image.

# Running
Io run use the command `docker run -d -p <port>:5000 <repository>` where `<port>` is the port you want to bind, `5000` is the container port that is being bound to, and `repository` is the same identifier used when building the image.

