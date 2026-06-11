FROM eclipse-temurin:21-jdk

RUN apt update && apt install -y git maven

WORKDIR /app

RUN git clone https://github.com/kairamumasatyasubhash/splunk-calculator.git

WORKDIR /app/splunk-calculator/calculator

RUN mvn clean package

EXPOSE 8081

CMD ["java","-jar","target/calculator-0.0.1-SNAPSHOT.jar"]
