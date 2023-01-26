# Vote App Frontend 

This is a frontend app, part of [Example Voting App](https://github.com/schoolofdevops/example-voting-app).  

To build and run this app as a container, 

  * use `python:alpine3.17` container base image
  * map/expose `container port 80`
  * copy over the source code 
  * run `pip install -r requirements.txt` to install dependencies
  * launch the app with `gunicorn app:app -b 0.0.0.0:80` command

  
### Building the Docker image
```bash
$ docker image build -t <image-name> .
$ docker run -p 80:80 -d <image-name>
```

### Push to DockerHub
```bash
$ docker login
$ docker tag <image-name> <docker-hub-name>/<image-name>
$ docker push <docker-hub-name>/<image-name>
```

<img width="1287" alt="image" src="https://user-images.githubusercontent.com/49791498/214632753-2368fd01-6b51-4bcd-b1ea-760914ca06a2.png">
