FROM java:8-jre
WORKDIR usr/src
ENV MONGO_DATABASE=ReminderServiceDB
ENV MONGO_URL=mongodb://mongocontainer:27018/ReminderServiceDB
ADD ./target/docker-reminder-service.jar /usr/src/docker-reminder-service.jar
EXPOSE 8081
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongocontainer:27017/ReminderServiceDB","-jar","/usr/src/docker-reminder-service.jar"]