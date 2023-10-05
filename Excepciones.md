# Excepciones
## Clase Throwable
Clase Madre de todas las excepciones. 
Todas heredan el atributo message.
Tambien contienen el atributo cause.
### 3 metodos
printStackTrace, traza de errores.
## Clases Exception y Error
Error: indican problemas graves que una app no deberia tratar de detectar. Son anormales
Exception: Errores logicos de sofware. Importantes
### Exception.

#### RuntimeException

Excepciones que normalmente surgen en programas, Logicos como dividir por cero. NullPonterException. o fuera de limites de indices

#### IO InputOutput
Flujo de datos externas las generan

#### SQLException
Conexion a DDBB fallos de query

#### AwtException

## Excepciones Unchecked
el compilador no es tan rigido, y no obliga a tratar especificamente. No es necesario poner un try-catch, ni tampoco la clausula 'throws'

## Excepciones Checked
Compilador rigido, pide explicitamente que hagamos algo con esa excepcion. Necesario agregar clausula 'throws'
