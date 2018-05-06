# containerization
Docker
- Images are read only templates used to create containers
- If an image is a class then a container is an instance of a class (a runtime object)
- Containers are lightweight and portable encapsulations of an envirnoment in which we can run our appplications
- In summary Container = Images (binaries + dependencies)
- You can have many containers running off the same image
- Containers are just processes

#### Starting a container - sample commands
`docker container run -d -p 3306:3306 --name db -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql`






#### Inspired by
[Play with Docker classroom](https://training.play-with-docker.com/ops-stage1/)
