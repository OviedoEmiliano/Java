# Despligue de Aplicaciones

3 Formas

## Applets
No Utiliza metodo main sino metodo init. Se ejecuta en el navegador. Algunos IDE proporcionan el appletviewer

    public void init(){
      JLabel rotulo = new JLabel("Hola mundo");
      add(rotulo);
    }

se crea una pag web en la carpeta /bin dentro del proyecto.

    <applet code="mis_applets/Hola_alumnos.class" width="500" height="500">
    </applet>

Debido a Hackeos la seguridad de los applets aumento, entonces es necesario agregar el sitio
configurar java > editar lista de sitios > agregar "file:/"
Al ejecutar la web salen mensajes de confirmacion de seguridad. Los cuales se pueden modificar
