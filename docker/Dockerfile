FROM maven:3.6.3-ibmjava-8-alpine as builder
WORKDIR /app
COPY . .
RUN mvn clean package
WORKDIR /app/webapp
CMD ["mvn", "jetty:run"]

# FROM openjdk:8-jre-alpine
# WORKDIR /app
# COPY --from=builder /app/target/openmrs-2.5.0-SNAPSHOT-tests.jar /app