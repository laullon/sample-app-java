FROM java:8-jdk-alpine

COPY target/printing-0.9.0-SNAPSHOT.jar /usr/app/
COPY app_k8s.yaml /usr/app/printing/
COPY applicationTags.yaml /usr/app/printing/
COPY wfReportingConfig.yaml /usr/app/

WORKDIR /usr/app

EXPOSE 50052

ENTRYPOINT ["java", "-jar", "printing-0.9.0-SNAPSHOT.jar", "./printing/app_k8s.yaml"]
