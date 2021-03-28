# ppt [dockerfile.pptx](https://github.com/s108000389/109-2--/files/6217626/dockerfile.pptx)

# java
### Dockerfile
```
FROM java:9

WORKDIR /app

COPY . /app

ENV PATH=$PATH:JAVA_HOME/bin
ENV JRE_HOME=${JAVA_HOME}/jre
ENV CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib

RUN ["javac","hello.java"]

ENTRYPOINT ["java","hello"]
```
### hello.java
```
import java.util.*;

public class hello{ 
public static void main(String[] args) { 

	System.out.println("Hello World");

	System.out.println(new Date());

	}
}
```

# python
### Dockerfile
```
FROM python:3.8.5

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN pip install -r requirements.txt


EXPOSE 5000
CMD ["python3", "/app/main.py"]
```
### main.py
```
print('Hello World!')
```
### requirement.txt
```
Flask
```

# node.js
### dockerfile
```
FROM node:8.9-alpine

EXPOSE 80

COPY . .

ENTRYPOINT ["node","node.js"]
```
### node.js
```
const http = require('http');

const port = 80;

const server = http.createServer((req, res) => {

 res.statusCode = 200;

 res.setHeader('Content-Type', 'text/plain');

 res.end('Hello World !');

})

server.listen(port);
```
