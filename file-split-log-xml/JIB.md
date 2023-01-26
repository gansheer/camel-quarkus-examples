# Notes on JIB tests

Added jib extension

Command to build:
mvn package -Pnative -DskipTests -Dquarkus.native.native-image-xmx=6144m -Dquarkus.container-image.builder=jib -Dquarkus.container-image.push=true -Dquarkus.container-image.registry=localhost:5000 -Dquarkus.container-image.insecure=true

Run not working for the following reason:
2023-01-26 10:24:34,628 ERROR [io.qua.run.Application] (main) Failed to start application (with profile [prod]): java.io.FileNotFoundException: src/main/resources/routes/camel-routes.xml does not exists

=> expected error
