# nginxDockerApp
Docker-Compose project

This will launch a python webapp and a static website.

Setup:
- The first thing that you want to do is to make sure that ports 80 and 5000 are open on the server that you are launching this on. 
- Secondly, install [docker](https://docs.docker.com/get-docker/) and [docker compose](https://docs.docker.com/compose/install/).
- Next, move everything into one directory and create a subdirectory called nginx, move the index.html into that directory. 
- Before you launch it, on the nginx.conf file, on line 14 replace "REPLACE_ME_WITH_SERVER_IP" with your server IP address.
- Finally, enter "docker-compose up" to launch the project.

Containers:
This will launch the following four containers: 
- A flask web app running the app.py that records and displays the site visitor count.
- A redis database for the app to use.
- A nginx web server to host the static website.
- A nginx reverse proxy to direct between the two pages.

You get directed between the static webpage and the flask app depending on if you requested /app or /static.

Disclaimer: The python app used is a sample app.
