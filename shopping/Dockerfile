FROM java:8-jdk-alpine

COPY target/shopping-0.9.0-SNAPSHOT.jar /usr/app/
COPY app_k8s.yaml /usr/app/shopping/
COPY applicationTags.yaml /usr/app/shopping/
COPY wfReportingConfig.yaml /usr/app/

WORKDIR /usr/app

EXPOSE 50150
EXPOSE 50050

ENTRYPOINT ["java", "-jar", "shopping-0.9.0-SNAPSHOT.jar","server", "./shopping/app_k8s.yaml"]
