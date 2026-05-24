MyBatis JPetStore
=================

[![Java CI](https://github.com/mybatis/jpetstore-6/actions/workflows/ci.yaml/badge.svg)](https://github.com/mybatis/jpetstore-6/actions/workflows/ci.yaml)
[![Container Support](https://github.com/mybatis/jpetstore-6/actions/workflows/support.yaml/badge.svg)](https://github.com/mybatis/jpetstore-6/actions/workflows/support.yaml)
[![Coverage Status](https://coveralls.io/repos/github/mybatis/jpetstore-6/badge.svg?branch=master)](https://coveralls.io/github/mybatis/jpetstore-6?branch=master)
[![License](https://img.shields.io/:license-apache-brightgreen.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

![mybatis-jpetstore](https://mybatis.org/images/mybatis-logo.png)

JPetStore 6 es una aplicación web completa construida sobre MyBatis 3, Spring 5 y Stripes.

Aspectos esenciales
-------------------

* [Ver la documentación](http://www.mybatis.org/jpetstore-6)

## Otras versiones que puede que quieras conocer

- JPetstore sobre Spring, Spring MVC, MyBatis 3 y Spring Security https://github.com/making/spring-jpetstore
- JPetstore con Vaadin y Spring Boot con Java Config https://github.com/igor-baiborodine/jpetstore-6-vaadin-spring-boot
- JPetstore sobre MyBatis Spring Boot Starter https://github.com/kazuki43zoo/mybatis-spring-boot-jpetstore

## Ejecutar en un servidor de aplicaciones
Ejecución del ejemplo JPetStore en Tomcat (usando el [cargo-maven2-plugin](https://codehaus-cargo.github.io/cargo/Maven2+plugin.html)).

- Clona este repositorio

  ```
  $ git clone https://github.com/mybatis/jpetstore-6.git
  ```

- Construye el archivo WAR

  ```
  $ cd jpetstore-6
  $ ./mvnw clean package
  ```

- Arranca el servidor Tomcat y despliega la aplicación web

  ```
  $ ./mvnw cargo:run -P tomcat90
  ```

  > Nota:
  >
  > Proporcionamos perfiles de Maven por servidor de aplicaciones como se indica a continuación:
  >
  > | Perfil         | Descripción |
  > | -------------- | ----------- |
  > | tomcat9        | Ejecución en Tomcat 9.0 |
  > | tomee80        | Ejecución en TomEE 8.0 (Java EE 8) |
  > | wildfly26      | Ejecución en WildFly 26 (Java EE 8) |
  > | liberty-ee8    | Ejecución en WebSphere Liberty (Java EE 8) |
  > | jetty          | Ejecución en Jetty 12 (Java EE 8) |
  > | glassfish5 (deshabilitado) | Ejecución en GlassFish 5 (Java EE 8) |
  > | payara5        | Ejecución en Payara 5 (Java EE 8) |
  > | resin          | Ejecución en Resin 4 |

- Ejecuta la aplicación en el navegador http://localhost:8080/jpetstore/
- Pulsa Ctrl-C para detener el servidor.

## Ejecutar en Docker
```
docker build . -t jpetstore
docker run -p 8080:8080 jpetstore
```
o con Docker Compose:
```
docker compose up -d
```

## Probar los tests de integración

Ejecuta los tests de integración de transición entre pantallas.

```
$ ./mvnw clean verify -P tomcat9
```
