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
  2. Virtualization on top of OS and not Physical resources
  3. Isolation and portability, reproducing consistent environment and outputs
  
#### A Simple add function using Flask

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
