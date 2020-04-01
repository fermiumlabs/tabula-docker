# Tabula on Docker

[Tabula](http://tabula.technology/) is a tool for liberating data tables trapped inside PDF files. This is a [Docker](https://docker.com) image to run the webserver inside a lightweight Linux container.

## Run from [Docker Hub](https://hub.docker.com/)

```
docker run -d -p 8080:8080 fermium/tabula
```

Now open your browser to http://localhost:8080/

### Run options

You may wish to tweak the `docker run` command above in order to...

- listen on a different port

  ```
  # Example: port 8100
  docker run -d -p 8100:8080 fermium/tabula
  ```

  Access the web interface at http://localhost:8100/

- follow the logs while the container runs

  ```
  docker run -p 8080:8080 fermium/tabula
  ```

You may find more options in the official [documentation](https://docs.docker.com/engine/reference/commandline/run/)

## Build your own image

Instead of pulling a pre-built container image from [fermium/tabula](https://hub.docker.com/r/fermium/tabula/), you may build your own using the Dockerfile in this repo:

```
git clone git@github.com:fermium/tabula-docker.git
docker build -t . tabula-docker
docker run -d -p 8080:8080 mytabula
```

