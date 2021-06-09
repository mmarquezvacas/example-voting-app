FROM maven:3.8.1-ibmjava-8-alpine
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests && \
    mv target/worker-jar-with-dependencies.jar /run/worker.jar && \ 
    rm -rf *
CMD java -jar /run/worker.jar