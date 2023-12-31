# Collection.
Estructuras dinamicas. Metodos comunes: Añadir, Eliminar obtener tamaño...

## Listas
Tienen Orden, Hijas de clase Collection
Pueden Tener Orden FIFO, y Orden LIFO

### ArrayList
- Matriz dinamica, Hereda de la clase AbstractList, la cual implementa la interfaz List
- Permite Colecciones o elementos duplicados
- Orden FIFO
- Tiene acceso aleatorio.(Indice)
- Manipulacion lenta.

Declaracion: List<Object> "Nombre" = new ArrayList<Object>();
Añadir: Metodo add
Tamaño: Metodo size
Traer Objeto: Metodo get

### LinkedList
- Lista doblemente enlazada
- Permite Duplicados
- Orden FIFO - SIN INDICE
- Manipulacion Rapida
- Se puede tratar como Pila o cola
- Insercion/Eliminacion Al principio o al final

Declaracion: List<Object> "Nombre" = new LinkedList<Object>();
Añadir: Metodo add. Recibe parametro de posicion
Tamaño: Metodo size
Traer Objeto: Metodo get. getFirst y getLast

### Stacks
Orden LIFO
Declaracion: Stack<Object> "Nombre" = new Stack<Object>();
Añadir: Metodo push
Buscar Elemento: Search(Indice). Metodo Peek Ultimo elemento Agregado
Eliminar Ultimo Registro: Metodo Pop

## Mapas/Diccionarios
- Añadir Elementos, pero se puede asignar una llave

### HashMap
- Selecciona el ultimo objeto añadido, en caso de misma key
- No Garantiza ningun orden especifico
Declaracion: Map<Key,Objeto> "Nombre" = new HashMap<Object>();
Añadir: Metodo put(Key,Objeto)
Recorrer: for(Entry<Key,Objeto> entry : diccionarioHash.entrySet())

### TreeMap
- Selecciona el ultimo objeto añadido, en caso de misma key, pero los ordena ascendentemente por key
Declaracion: Map<Key,Objeto> "Nombre" = new TreeMap<Object>();
Añadir: Metodo put(Key,Objeto)
Recorrer: for(Entry<Key,Objeto> entry : diccionarioTree.entrySet())

 ### LinkedHashMap
 - Selecciona el ultimo objeto añadido, en caso de misma key
 - Se almancenan por orden de insercion
Declaracion: Map<Key,Objeto> "Nombre" = new TreeMap<Object>();
Añadir: Metodo put(Key,Objeto)
Recorrer: for(Entry<Key,Objeto> entry : diccionarioTree.entrySet())
