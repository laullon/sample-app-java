FROM java:8-jdk-alpine

COPY target/delivery-0.9.0-SNAPSHOT.jar /usr/app/
COPY app_k8s.yaml /usr/app/delivery/
COPY applicationTags.yaml /usr/app/delivery/
COPY wfReportingConfig.yaml /usr/app/

WORKDIR /usr/app

EXPOSE 50054

ENTRYPOINT ["java", "-jar", "delivery-0.9.0-SNAPSHOT.jar", "--spring.config.location=/usr/app/delivery/app_k8s.yaml"]

