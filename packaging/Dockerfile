FROM java:8-jdk-alpine

COPY target/packaging-0.9.0-SNAPSHOT.jar /usr/app/
COPY app_k8s.yaml /usr/app/packaging/
COPY applicationTags.yaml /usr/app/packaging/
COPY wfReportingConfig.yaml /usr/app/

WORKDIR /usr/app

EXPOSE 50053

ENTRYPOINT ["java", "-jar", "packaging-0.9.0-SNAPSHOT.jar", "./packaging/app_k8s.yaml"]
