# webfortune

![example workflow](https://github.com/Joverkamp/webfortune/actions/workflows/python-app.yml/badge.svg)

This program allows users to communicate to a linux command line via webserver to receive fortunes, use cowsay, and a combination of both.

### Web commands

`<ip>:<port>/fortune/` - gives you a random fortune.

`<ip>:<port>/cowsay/<message>/` - cow says message you give it.

`<ip>:<port>/cowfortune/` - cow tells you a random fortune.


# Running with Docker

### Building

To build this application you must have docker installed. Then to create your docker image, run this command `docker build -t <repository> .` where `<repository>` is how you want to identify your docker image.

### Running

Io run use the command `docker run -d -p <port>:5000 <repository>` where `<port>` is the port you want to bind, `5000` is the container port that is being bound to, and `repository` is the same identifier used when building the image.

### Stop running

To stop running your docker container first run this command `docker ps`. Lookfor the image with your unique identifier and copy its container id. Then run this command to stop the container `docker stop <container id>`.

# Running Locally

### Set up your environment

To set your environment follow these commands.

  `python3 -m virtualenv env`

  `source env/bin/activate`

  `pip3 install -r requirements.txt`

### Testing

Before you run the application, test it by running this command `pytest`.

### Running

To run the webserver and type `FLASK_APP=appserver.py flask run --host=0.0.0.0`. Then in the browser of your choice type `<your_ip_address>:5000`.


