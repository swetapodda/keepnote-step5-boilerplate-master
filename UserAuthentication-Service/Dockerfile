FROM java:8-jre
WORKDIR usr/src
ENV MYSQL_DATABASE=ReminderServiceDB
ENV MYSQL_URL=mongodb://mongocontainer:27018/NoteServiceDB
ADD ./target/docker-auth-service.jar /usr/src/docker-auth-service.jar
EXPOSE 8089
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongocontainer:27017/CategoryServiceDB","-jar","/usr/src/docker-auth-service.jar"]