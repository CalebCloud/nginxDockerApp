# nginxDockerApp
Docker-Compose project

This will launch a python webapp and a static website.

Setup: 
- install [docker](https://docs.docker.com/get-docker/) and [docker compose](https://docs.docker.com/compose/install/).
- enter "docker-compose up" to launch the project.

Containers:
This will launch the following four containers: 
- A flask web app running the app.py that records and displays the site visitor count.
- A redis database for the app to use.
- A nginx web server to host the static website.
- A nginx reverse proxy to direct between the two pages.

You get directed between the static webpage and the flask app depending on if you requested /app or /static.
