# Spring MVC
Marco web construido soble la pila de Java Servlet. Simplifica el desarrollo de apps web que se ejecutan en contenedores de servlets
Esta incluido en el starter-web
* Patrones de diseños Dispatcher Servlet y Modelo Vista Controlador
* Asignacion de controladores, controladores anotados
* Manejo de Formularios y validacion de formularios
* 
## Modelo Vista Controlador
* Controlador: Recibe peticiones del cliente. No se comunica directamente con la DDBB, sino se comunica con el modelo. Una vez recibido los datos los envia a la vista
* Modelo: Se Comunica con la base de datos. Y le envia al controlador los datos
* Vista: Interactua con el cliente, Muestra los datos
* 
## Capas de Spring MVS
* Presentacion: "Vista". @Controller recibe peticiones y las envia a negocio. Una vez terminado el ciclo y obtenidos los datos los muestra por la vista
* Negocio: @Services, operaciones de negocio
* Acceso a datos: @Repository, interactua con los datos, tiene acceso a la DDBB

### Estereotipos: 
@Component: Componente de Spring. Indica a Spring que esa clase cumple cierta funcion
Son aquellas anotaciones que extienden de otra anotacion
define un conjunto de anotaciones que categorizan cada uno de los componentes asonciandoles una responsabilidad concreta
*@Repository:Se encarga de dar de alta un bean. ese bean va a interactuar con la DDBB
Bean: Componente o elemento de spring
*@Service: se encarga de gestionar las operaciones de negocio a nivel de la aplicacion. y aglutina llamadas a varios repositorios de forma simultanea.
Su tarea fundamental es la de agregador, implementa el patron fachada y aglutina varios repositorios y llamadas a otros servicios{
@Controller: realiza la tarea de controlador y gestion de la comunicacion entre el usuario y el aplicativo. se apoya habitualmente en algun motor de plantillas o librerias de etiquetas que facilitan la creacion de paginas
