FROM java:8-jre
WORKDIR usr/src
ENV MONGO_DATABASE=CategoryServiceDB
ENV MONGO_URL=mongodb://mongocontainer:27018/CategoryServiceDB
ADD ./target/docker-category-service.jar /usr/src/docker-category-service.jar
EXPOSE 8083
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongocontainer:27017/CategoryServiceDB","-jar","/usr/src/docker-category-service.jar"]