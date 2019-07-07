Config and Discovery Repository Example
------------------------------------------------------------------------------------------------------------------------

Repositorio de ejemplo para leer configuración de microservicios desde un servicio Config Server
desarrollado con Spring Boot y Spring Cloud.

Estas configuraciones son leidas desde el proyecto "Spring Cloud Config/Discovery Example":

  https://github.com/edgar-code-repository/spring-cloud-config-example

------------------------------------------------------------------------------------------------------------------------

**Configuración para el servicio eureka-service:**

El servicio eureka-service debe correr en el puerto 9999.

```
  server.port=9999
  eureka.client.register-with-eureka=false
  eureka.client.fetch-registry=false

```

------------------------------------------------------------------------------------------------------------------------

**Configuración para el servicio movie-info-service:**

El servicio movie-info-service debe correr en el puerto 5501.
Se define el string message y la url donde corre el servicio eureka.

```
  server.port=5501
  message=Hello World!!! This is a message read from git using the config service!!!
  eureka.client.serviceUrl.defaultZone=http://localhost:9999/eureka/

```

------------------------------------------------------------------------------------------------------------------------
