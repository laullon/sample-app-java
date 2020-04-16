FROM java:8-jdk-alpine

COPY target/styling-0.9.0-SNAPSHOT.jar /usr/app/
COPY app_k8s.yaml /usr/app/styling/
COPY applicationTags.yaml /usr/app/styling/
COPY wfReportingConfig.yaml /usr/app/

WORKDIR /usr/app

EXPOSE 50051

ENTRYPOINT ["java", "-jar", "styling-0.9.0-SNAPSHOT.jar","server", "./styling/app_k8s.yaml"]
