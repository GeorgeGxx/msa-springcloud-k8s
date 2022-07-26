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

`Comandos Docker`

docker build -t usuarios .
docker build -t usuarios . -f .\msvc-usuarios\Dockerfile

docker images
docker ps -a

docker run -p 8001:8001 usuarios
docker run -d -p 8001:8001 nombre_usuarios // -d detach corre un contenedor en segundo plano
docker start nombre_contenedor // Lo inicia si ya esta creado con detach

docker stop zen_zhukovsky o 1b3 // Detiene el contenedor por nombre o por id

docker rmi // Elimina imagen
docker image prune // Elimina todas las imagenes que no se usan

docker rm // Elimina contenedor
docker container prune // Elimina todos los contenedores que no se usan

docker attach nombre_contenedor // Accede al contenedor, para ver los logs en tiempo real
docker logs nombre_contenedor o id // Muestra logs del contenedor
docker attach -f nombre_contenedor // -f para conectarte al contenedor en ejecucion persistente, sigue la salida

docker --help // Muestra ayuda
docker image --help
docker container --help
docker network --help
docker run --help

