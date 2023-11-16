# Instalacion Para Conectar Una Base de Datos SQL Server Con Java
1- Descargar conector, verificar version de java, SQL server e IDE
2- Libraries -> Add JAR File
3- Activar Puerto 1433
  a- Sql Server Configuration Manager
  b- Sql Server Network Configuration
  c- Protocols
  d- Enable TCP/IP

## Crear Clase de Conexion

Public static Connection getConexion(){
  String conexionUrl = "jdbc:sqlserver://localhost:1433;"
          + "database=name;"
          + "user=sa;"
          + "password=xxxxxx;"
          + "loginTimeout=time;"; - Parametro Adicional, tiempo que tarda en procesar la conexion.
  
  try{
    Connection conn = DriverManager.getConnection(conexionUrl);
    return conn;
  } catch(SQlException ex){
    System.out.println(ex.toString());
    return null;
  }
}

## Realizar Consulta
-Clase PreparedStatement, Revisar Datos de una Tabla y Agregar/Borrar/Modificar. Mayor Flexibilidad que Statement, en consultas se puede utilizar el '?'

try{
  conn = Conexion.getConexion();
  PreparedStatement ps = conn.prepareStatement("SELECT * FROM 'table' WHERE id = ? ")
  ps.setInt(1,1);. Int porque ID es entero, sino otro tipo de dato.
  rs = ps.executeQuery();
  
  while(rs.next()){
    //Mostrar Cada Columna de la Tabla
  }
}catch(SQLException e){
  System.out.println(e.toString());

}
