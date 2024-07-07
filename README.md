
# LiterAlura

LiterAlura es una aplicación de consola que permite gestionar un catálogo de libros. Los usuarios pueden registrar libros en una base de datos y recibir información sobre los libros registrados. Este proyecto utiliza tecnologías como Java, Spring Boot y PostgreSQL.

## Funcionalidades

La aplicación proporciona las siguientes funcionalidades:
1. Buscar libro por título y registrarlo en la base de datos.
2. Listar libros registrados.
3. Listar autores registrados.
4. Listar autores vivos en un determinado año.
5. Listar libros por idioma.

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:
- Java 17
- Maven
- PostgreSQL

## Configuración del Proyecto

### Clonar el Repositorio

Clona el repositorio del proyecto a tu máquina local:

```sh
git clone https://github.com/tu_usuario/literalura.git
cd literalura
```

### Configurar la Base de Datos

Asegúrate de tener una base de datos PostgreSQL creada. Puedes crearla utilizando `pgAdmin` o la línea de comandos de PostgreSQL:

```sql
CREATE DATABASE gutendex_menu_db;
```

### Configurar las Propiedades de la Aplicación

Configura las credenciales de tu base de datos en el archivo `src/main/resources/application.properties`:

```properties
spring.application.name=gutendex_menu

spring.datasource.url=jdbc:postgresql://localhost:5432/gutendex_menu_db
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.datasource.driver-class-name=org.postgresql.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

### Construir el Proyecto

Utiliza Maven para construir el proyecto:

```sh
mvn clean install
```

## Ejecutar la Aplicación

Para ejecutar la aplicación, usa el siguiente comando:

```sh
mvn spring-boot:run
```

La aplicación se ejecutará en la consola y mostrará un menú con las opciones disponibles.

## Uso de la Aplicación

### Menú Principal

La aplicación mostrará el siguiente menú en la consola:

```
1 - Buscar libro por título para registrarlo en la base de datos
2 - Listar libros registrados
3 - Listar autores registrados
4 - Listar autores registrados vivos en un determinado año
5 - Listar libros registrados por idioma
0 - Salir
```

### Buscar Libro por Título

Selecciona la opción `1` e ingresa el título del libro que deseas buscar. La aplicación consultará la API de Gutendex y registrará el libro en la base de datos si no está registrado.

### Listar Libros Registrados

Selecciona la opción `2` para listar todos los libros registrados en la base de datos.

### Listar Autores Registrados

Selecciona la opción `3` para listar todos los autores registrados en la base de datos.

### Listar Autores Vivos en un Determinado Año

Selecciona la opción `4` e ingresa el año que deseas consultar. La aplicación listará todos los autores que estaban vivos en ese año.

### Listar Libros por Idioma

Selecciona la opción `5` e ingresa el código del idioma (por ejemplo, `es` para español, `en` para inglés, etc.). La aplicación listará todos los libros registrados en ese idioma.

### Salir

Selecciona la opción `0` para salir de la aplicación.

## API Utilizada

La aplicación consume datos de la API de Gutendex, que proporciona información sobre libros del Proyecto Gutenberg. Puedes encontrar más información sobre la API en [Gutendex](https://gutendex.com/).


