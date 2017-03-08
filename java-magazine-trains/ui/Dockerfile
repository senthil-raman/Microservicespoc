FROM java:openjdk-8u45-jdk


RUN mkdir /app

WORKDIR /app

ADD . /app

RUN mvn clean package

ENV JAVA_ENV=PRODUCTION

EXPOSE 8080

CMD ["java", "-server", "-cp", "ui/target/classes:ui/target/dependency/*", "com.kumuluz.ee.EeApplication"]