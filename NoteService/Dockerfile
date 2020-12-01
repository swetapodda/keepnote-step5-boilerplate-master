FROM java:8-jre
WORKDIR usr/src
ENV MONGO_DATABASE=NoteServiceDB
ENV MONGO_URL=mongodb://mongocontainer:27018/NoteServiceDB
ADD ./target/docker-note-service.jar /usr/src/docker-note-service.jar
EXPOSE 8082
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongocontainer:27017/NoteServiceDB","-jar","/usr/src/docker-note-service.jar"]