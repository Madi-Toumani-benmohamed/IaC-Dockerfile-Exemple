FROM openjdk:10 as build 
COPY . /usr/src/myapp

WORKDIR /usr/src/myapp 

RUN javac Main.java 


FROM openjdk:10-jre-slim 
COPY --from=build /usr/src/myapp/Main.class /usr/src/myapp/
WORKDIR /usr/src/myapp 
CMD [ "java", "Main" ]
