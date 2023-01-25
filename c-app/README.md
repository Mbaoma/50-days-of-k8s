# Facebooc

Proof-of-concept Facebook clone in C.
The only dependency is SQLite3.

# Prerequisites

**OS: Ubuntu**

Install following  package:  

  * build-essential
  * make
  * libsqlite3-dev
  * sqlite3
  
```bash
sudo apt-get update
sudo apt-get install -yq build-essential make libsqlite3-dev sqlite3
```
**Note**: When you launch a container using **ubuntu** image from the repository, it may not have sudoers installed. Also, you would be a root user inside the container. In such case, remove sudo and execute rest of the command. 


# Build

Using git, clone the repository with the URL above. Repository contains the source files written in C, along with a Makefile with targets such as "all", "run". Destination path should be **/opt/facebooc**.
Run the following command to compile the source code.make all

```bash
cd facebooc
make all
```

# Run 

Launch app as bin/facebooc This will attach to port **16000**


```bash
cd facebooc
bin/facebooc
```



Licensing
---------
`Facebooc` is freely redistributable under the two-clause BSD License.
Use of this source code is governed by a BSD-style license that can be found
in the `LICENSE` file.

  
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
<img width="1287" alt="image" src="https://user-images.githubusercontent.com/49791498/214644459-8b713b9d-0680-494d-a6c1-d6a7c06c2bce.png">
