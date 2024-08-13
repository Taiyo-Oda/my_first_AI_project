FROM openjdk:17-jdk-slim
RUN apt-get update && apt-get install -y maven
WORKDIR /src
COPY pom.xml .
COPY src ./src
RUN mvn clean package -DskipTests
CMD ["java", "-jar", "target/backend-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080