# JDBC Java Database Connectivity
Api que permite conectarse a base de datos estandar SQL, proporciona un acceso uniforme a una gran variedad de DDBB relacionales.
* Establece una conexion con la base de datos
* Envia Sentencias SQL
* Procesa los resultados

## Statement - ResultSet
    private void consulta() throws SQLException{
      Statement statement = new conexion.createStatement();
      ResultSet set = statement.executeQuery(//query//);
      while(set.next()){
        /* EJEMPLO
        int idAlumno = set.getint("id_alumno");
        String nombre = set.getString("nombre");
        */
      }
      set.close();
      statement.close();
    } 
## PreparedStatement
Es mas seguro

     private void consulta() throws SQLException{
          String query = "SELECT * FROM alumnos where nombre = ?";
          PreparedStatement statement = new conexion.PreparedStatement(query);
          statement.setString(1, "nombre")
          ResultSet set = statement.executeQuery();
          while(set.next()){
            /* EJEMPLO
            int idAlumno = set.getint("id_alumno");
            String nombre = set.getString("nombre");
            */
          }
          set.close();
          statement.close();
        } 

##Transacciones
Decir a SQl que ejecute transacciones como un solo bloque ("BEGIN"-"COMMIT"). Motor InnoDB de MySQL soporta transacciones.
avisar a jdbc que vas a utilizar modo transaccional con "conexion.setAutoCommit(false)"
palabra clave final, significa que la clase no puede tener subclases, la herencia esta prohibida. util cuando se crean objetos inmutables

    private void conectar() throws SQLException {
        string jdbc = "jdbc:mysql://localhost:3306/ejemplo";
        conexion = DriverManager.getConnection(jdbc, "user", "password"); 
        conexion.setAutoCommit(false);
    }
    
    private void transaccion(){
          final String PROFESOR = "INSERT INTO profesores(id, nombre) VALUES(?,?)";
          final String ALUMNO = "INSERT INTO alumnos(id, nombre) VALUES(?,?)";
          PreparedStatement profesor, alumno;
          try{
            profesor = conexion.preparedStatement(PROFESOR);
            profesor.setInt(1,50);
            profesor.setString(2,"Juan");
            // NO SE UTILIZA EXECUTEQUERY, SINO EXECUTEUPDATE
            profesor.executeUpdate();

            alumno = conexion.preparedStatement(ALUMNO);
            alumno.setInt(1,50);
            alumno.setString(2,"Juan");
            // NO SE UTILIZA EXECUTEQUERY, SINO EXECUTEUPDATE
            alumno.executeUpdate();

            conexion.commit():
          } catch(SQLException e){
            conexion.rollback();
            e.printStackTrace();
          } finally {
            if (profesor != null){
            profesor.close();
            }
            if (alumno != null){
            alumno.close();
            }
          }
          
    }
