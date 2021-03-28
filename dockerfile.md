## ppt [dockerfile.pptx](https://github.com/s108000389/109-2--/files/6217626/dockerfile.pptx)

## java
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
