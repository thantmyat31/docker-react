#### Build docker image
$ docker build -f Dockerfile.dev .

#### Run react frontend in docker
$ docker run -it -p 3000:3000 [ IMAGE ]

#### Run react frontend in docker by mapping volume from local machine
**For windows OS** <br />
$ docker run -it -p 3000:3000 -v /app/node_modules -v ${PWD}:/app -e CHOKIDAR_USEPOLLING=true [ IMAGE ]

**For others OS** <br />
$ docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app [ IMAGE ]

#### Run react frontend static UI on Nginx server as docker image
$ docker run -p 8080:80 [ IMAGE ]