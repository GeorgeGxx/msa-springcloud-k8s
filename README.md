# SpringCloud Microservices on Kubernetes

Powered by Java 11 & SpringBoot

Notas:

`Empaquetar .jar`

Moverte al nivel del pom.xml

.\mvnw clean package

.\mvnw clean package -DskipTests

`Ejecutar .jar`

java -jar .\target\msvc-usuarios-0.0.1-SNAPSHOT.jar

java -jar .\target\msvc-cursos-0.0.1-SNAPSHOT.jar

`Enpoint & Request`

- localhost:8001

{
"nombre": "Jorge",
"email": "jorge@correo.com",
"password": "12345"
}

- localhost:8002

{
"nombre":"Kubernetes"
}

