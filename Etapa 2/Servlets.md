# Servlets
Clase Intermediaria entre JSP y un Server Web
Se encarga de recibir peticiones
## Metodos
### doGet(): 
Se encarga de recibir las solicitudes que provienen mediante GET. Recibir Info

HttpSession misesion = request.getSession();
misesion.setAttribute("listaUser", ListaUser)
response.sendRedirect("mostrarUsuarios.jsp");

<%
List<Usuario> listaUsuarios = (List) request.getSession().getAttribute("listaUsuarios");
for(Usuario usu : listaUsuarios){
%>
......................HTML..................
<%
}
%>

### doPost(): 
Se encarga de recibir las solicitudes que provienen mediante POST. Enviar Info

### getParameter(): 
Se utiliza para obtener el valor de un parametro enviado por el cliente mediante metodos GET o POST

EJ: String dato = request.getParameter("txtNombre")

