FROM private-registry-svc.default.svc.cluster.local:5000/openjdk11-apm:v0.0.1
MAINTAINER "gkim" <guardkim9@nate.com>

ENV JAVA_OPTS="-server -Xms128M -Xmx256M" \
    JAVA_OPTS_APPEND="-XX:+UseG1GC"

COPY basic-springboot-276/build/libs/ .

CMD ["java", "$JAVA_OPTS", "$JAVA_OPTS_APPEND", "-jar", "*.jar"]
