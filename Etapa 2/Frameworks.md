# Frameworks de Desarrollo Web
Entornos de Trabajo que incluyen un conjunto de herramientas y librerias que pueden ser utilziadas de forma sencilla 

## Spring
Conjunto de Proyectos OpenSource, para agilizar procesos de desarrollo de aplicaciones. Cuenta con uan cantidad de herramientas.

### Spring Boot
Deriva de Spring Framework, facilita el desarrollo web sin la necesidad de configuracion xml. Usa dependencias iniciales. Incluye su propio servidor "TomCat".

#### Starter
Mecanismo para simplificar el desarrollo de apps al proporcionar config y dependencias preconfiguradas.
- spring-boot-starter-parent: define valores predeterminados comunes, version de java, codificacion utf-8 y varias config de Maven para el desarrollo de Java Spring. Hereda la gestion de dependencias de spring-boot-dependencies
- spring-boot-starter-web: especifica dependencias para desarrollar aplicaciones web Java con Spring web MVC y servidor Tomcat
- spring-boot-starter-data-jpa: dependencias en Data JPA, juntos con las dependencias de la bilbioteca Hibernate

#### Spring Boot por Consola
@SpringBootApplication: Notacion que permite la funcionalidad de una clase, que es la principal.
- @EnableAutoConfiguration: Se encarga de intentar configurar Spring de forma automatica. Buscar en el class PATH todas las entidades
- @ComponentScan: Se encarga de revisar los paquetes actuales que tengan anotaciones de esteriotipo(Controller ,service, repository)
- @SpringBootConfiguration: indica que la clase notada es una fuente de definiciones de bins, te dice que una clase tiene una cierta cantidad de bins
@Entity: Entidad
@Controller
@Service:
@Repository
