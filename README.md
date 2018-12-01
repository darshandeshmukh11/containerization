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

#### Sample Dockerfile
```
# Use an official Python runtime as a parent image
FROM python:2.7-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]
```







#### Inspired by
[Play with Docker classroom](https://training.play-with-docker.com/ops-stage1/)
