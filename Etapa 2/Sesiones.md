# Sesiones
creadas para seguir y memorizar las acciones de un usuario en un sitio web
Se almacenan en la memoria del servidor

### Algunos metodos
setAttribute(name,object);
name: nombre significativo.
object: Objeto que quieres que se almacene en memoria.
getAttribute(name);
isNew();
getID();
invalidate();
setMaxInactiveInterval(time);

## EJEMPLO DE SESSION

    <ul>
    <%
        List<String> listaElementos = (List<String>)session.getAttribute("misElementos"); 
    
        if(listaElementos==null){
        listaElementos = new ArrayList<String>();
        session.setAttribute("misElementos",listaElementos);
        }
    
        String[] elementos=request.getAttributeValue("articulos");
        if (elementos != null){
          for (String elem : elementos){
            listaElementos.add(elemTemp)
          }
        }
        for (String elem : listaElementos){
          out.println("<li>" + elemTemp + "</li>");
        }
      %>
      </ul>
