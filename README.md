# Estrategias de Persistencia

### Universidad Nacional de Quilmes (UNQ)

## Descripción
Este repositorio contiene el proyecto final y el material práctico desarrollado durante la cursada de la materia "Estrategias de Persistencia". 

## Dominio
Nos situamos en una realidad alterna llamada Epersgeist, donde entidades como **Espíritus** y **Mediums**, se encuentran interactuando en distintas **Ubicaciones** y nosotros somos los encargados de persistir sus travesias. 

### Lore completo:
- [Entrega 1 - JDBC](enunciado/entrega1/entrega1.md)
- [Entrega 2 - ORM - Hibernate](enunciado/entrega2/entrega2.md)
- [Entrega 3 - ORM - Spring](enunciado/entrega3/entrega3.md)
- [Entrega 4 - NoSQL - Neo4j - Spring](enunciado/entrega4/enunciado_tp4.md)
- [Entrega 5 - NoSQL - MongoDB - Spring](enunciado/entrega5/enunciado_tp5.md)
- [Entrega 6 - NoSQL - Firebase - Spring](enunciado/entregaFinal/enunciadoFinal.md)

### Tecnologías utilizadas
- **Lenguaje:** Java 21
- **Framework:** Spring en conjunto con Spring Boot y Spring Web Flux
- **Programación reactiva:** Mono y Flux para manejo asíncrono de datos en tiempo real.
 Solo implementado en el proyecto final para potenciar la propiedad realtime de Firebase.
- **Bases de datos:**
  - Relacional: MySQL
  - NoSQL: MongoDB y Firebase
  - Base de grafos: Neo4J

## Contenidos abordados
A lo largo de la cursada se exploraron los siguientes conceptos y tecnologías:

### Persistencia y bases de datos
- **ORM y Hibernate:** Introducción y ciclo de vida de los objetos.
- **Teorema CAP:** Consistencia, disponibilidad y tolerancia a particiones.
- **Propiedades ACID:** Atomicidad, consistencia, aislamiento y durabilidad.
- **Tipos de permisos en bases de datos:** Read-Only, Read-Write, Write-Only, No-Access
- **Performance:**
  - Optimización de consultas para evitar cargar datos innecesarios en memoria.
  - Uso de índices y estrategias para consultas eficientes.
  

### Spring Framework
- Configuración del entorno y conexión a bases de datos.
- **Inyección de dependencias.**
- Manejo de **transacciones** en el contexto de una aplicación.

### Arquitectura y diseño
Se adoptó una arquitectura basada en **Clean Architecture** con las siguientes capas:
- **Controller:** APIs REST y manejo de DTOs.
- **Modelo:** Contiene la lógica de negocio.
- **Service:** Actúa como intermediario entre la lógica de negocio y la capa de persistencia.
- **Persistencia:**  Uso de DAOs para interactuar con las bases de datos.

### Herramientas y técnicas
- **Neo4J:** Introducción al uso de bases de grafos. Usado para recorrer nodos.
- **MongoDB:** Usado especicamente para consultas geo-espaciales.
- **Firebase:** Investigación e implementación como proyecto final.
- **Postman:** Testing de endpoints REST.
- **MockMVC:** Pruebas unitarias y de integración para APIs.

### Problemáticas abordadas
- **Concurrencia a nivel teorico:**
  - Lockeo optimista y pesimista.
  - Estrategias para manejar el acceso concurrente a las bases de datos.
- **Caché de segundo nivel (L2):** Uso y beneficios en Hibernate.
- **Problema de impedancia objeto-relacional:** Cómo resolver la transformación entre estructuras del programa y estructuras de la base de datos.
- **Estrategias de actualización:** Reachability y cascada.

### Testing
Se realizaron pruebas:
- **Unitarias:** A nivel de componentes individuales.
- **Integración:** Verificación del correcto funcionamiento entre diferentes módulos.
- **End-to-End:** Validación completa del flujo.

## Objetivos del curso
- **Conocer distintos mecanismos de persistencia** y realizar comparaciones prácticas.
- **Entender la interacción entre programas y mecanismos de persistencia.**
- **Explorar problemáticas específicas:**
  - Persistencia de objetos.
  - Concurrencia y performance.
  - Seguridad y manejo de permisos en bases de datos.

### Cómo ejecutar el proyecto
1. Clonar el repositorio.
   ```bash
   git clone <url_del_repositorio>
   ```
2. Configurar las bases de datos necesarias:
   - MySQL: Crear la base de datos y actualizar `application.properties` con las credenciales.
   - MongoDB: Asegurarse de que el servidor esté corriendo.
   - Neo4J: Proveer la URL y las credenciales.
   - Firebase: Descarga la key de Firebase y guardala en el directorio `resources` con el nombre `epers-key.json` 
3. Compilar y ejecutar la aplicación.
   ```bash
   ./gradlew bootRun
   ```
4. Acceder a la API a través de Postman o un navegador web en `http://localhost:8080`.

## IMPORTANTE
 -  Este proyecto fue un trabajo grupal durante toda la cursada. No puedo forkear el proyecto por eso cree el repo.
 -  Esta bajo licencia de uso academico, destinado a fines educativos y como muestra de los contenidos vistos en la materia.
 -  El proyecto fue evolucionando a la vez que veiamos contenidos nuevos. No hay rastros de herramientas como JDBC por ejemplo pero fue visto. 


