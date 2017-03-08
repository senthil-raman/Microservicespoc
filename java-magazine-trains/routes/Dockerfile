FROM java:openjdk-8u45-jdk



WORKDIR /app

ADD . /app

RUN mvn clean package -Pdeploy

ENV JAVA_ENV=PRODUCTION

EXPOSE 8080

CMD ["java", "-server", "-cp", "routes/target/classes:routes/target/dependency/*", "com.kumuluz.ee.EeApplication"]