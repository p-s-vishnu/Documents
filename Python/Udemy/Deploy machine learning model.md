## Deploy Machine learning models using docker containers

###  Intro

#### How to incorporate the model ?
  1. Making it as a Web service
  2. Incorporating to an existing software
  3. Automating existing workflows
  
#### Learning goals
  1. Introduction to Dockers
  2. Deploying ML solution using Docker container
  3. Build and deploy two ML services
  
#### Why Docker ?
  1. Provides standard environment, model instantiation and resource isolation.
  2. Virtualization on top of OS and not Physical resources.
  3. Isolation and portability, reproducing consistent environment and outputs
  
#### A Simple add function using Flask

Setup flask on Ubuntu : [Link](http://hanzratech.in/2015/01/16/setting-up-flask-in-ubuntu-14-04-in-virtual-environment.html)

  ```python
  # install flask 
  pip install flask
  
  from flask import Flask
  
  app = Flask(__name__)
  
  @app.route('/', methods=['GET', 'POST'])
  def add() :
    a = request.args.get("a")    
    b = request.args.get("b")
    
    return str( int(a) + int(b) )
    
  if __name__ == '__main__' :
  # This would start the service and return a URL
    app.run([port=PORT_NUM])
  ```
  
  > In order to test the function using a browser, enter the `URL?a=10&b=20`. It should return a value of 30 in browser.
  
  POST can be used in following cases - 
  * Secure data needs to be transferred, hiding from URL
  * Images and files are not supported by GET.
  
  Flasgger can be used to provide an UI for the model.
  
#### Writing and building docker file
  Docker FILE commands. 
  1. FROM : `BASE IMAGE` can be specified using the FROM command. Here we will be using continuumio/python image.
  2. COPY : `HOST ENVIRONMENT` files can be transferred to the `DOCKER` container. eg: scripts in the host environment can be transferred to docker and can be run there. 
  3. EXPOSE : Used to expose a PORT NUMBER to the outer environment.
  4. WORKDIR : working dir of the container when it starts
  5. RUN : All the required dependencies can be downloaded using it. eg :`RUN pip install 
  6. CMD : Similar to run command, this should be the last block. This must not terminate. eg : python flask1.py

  [Docker child commands](https://docs.docker.com/engine/reference/commandline/docker/)
  
  **Some docker commands**
  1. `docker commit` Creates an image from container's change.
  2. `docker diff`	Inspect changes to files or directories on a container’s filesystem
  3. `sudo docker search` The default registry is accessible.
  4. `sudo docker build -t IMAGENAME` Associate an image with a repository.
  5. `docker ps` lists all running container
  6. `docker diff` command has 3 events - 'A' A file or directory was added, 'D' A file or directory was deleted,'C' A file or directory was changed.
  
  `docker run -p <your_port> <docker_port> <name of image>`, used to start the conatainer. In our case, the Docker command will be `docker run -p 5000:5000 rf-api`
