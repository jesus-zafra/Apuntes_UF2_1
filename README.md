## M5-UF2-1 Optimitzación del Software
![jpg de bugs](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/bug.jpeg)
***
# Pruebas de software  
Consiste en probar que nuestros programas funcionan como deberían para conseguir que sea un software de calidad, o lo que es lo mismo, conseguir que desempeñen todo aquello que se pedía en sus especificaciones o requisitos descritos durante su fase de diseño de la mejor forma posible. Para ello se comprueban diferentes resultados dando al programa diferentes entradas y observando que los resultados son los esperados.  
![png frameworks](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/frameworks.png)
***
### Frameworks
Para facilitar el desarollo de las pruebas podemos usar *Frameworks*. Éstos son un entorno de desarrollo de software que unifica una serie de criterios, librerías y recursos de cara a programar de una forma estandarizada de forma que siguiendo esas pautas nos veamos todos obligados a utilizar buenas prácticas de programación y facilitan enormemente la comprensión del código entre todos los miembros participantes en un equipo de programación.  

En general, un *Framework* se compone de:
- **Reglas** o partes que obligan al cumplimiento de *buenas prácticas de programación*
- **Herramientas comunes**
- **Bibliotecas**
***
![jpg software testing](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/software-testing.jpeg)
### Tipos de pruebas
Las pruebas pueden ser:
- **Funcionales**
- **No funcionales**
***  
- **Pruebas Funcionales**  
  Sirven  para comprobar que todo funciona tal como se especificó en su diseño en base a los requisitos, o   especificaciones iniciales.  
  
  Hay varios tipos:  
  
  - *De unidad* (o *unitarias*)  
  Se realizan examinando cada unidad de código en el código fuente de la aplicación.
  Són las pruebas de más bajo nivel que se pueden realizar, normalmente las llevan a cabo los programadores.  

  - *De regresión*  
 Si se ha producido un cambio se mira que esto no afecte a la funcionalidad previa.  

  - *De integración* 
Una vez se han comprobado todas las unidades de código (pruebas unitarias) se realizan las pruebas de integración que verifican que todos los elementos unitarios que componen el programa funcionan correctamente probados en grupo.  

  - *De humo* (o *smoke test*)  
Revision rápida para comprobar que el producto funciona y no tiene defectos evidentes. Es una evaluación inicial de la calidad.  

  - *Alfa* y *Beta*  
Las pruebas Alfa son las pruebas que se le hacen al programa mientras todavía está en desarrollo. Las pruebas Beta son aquellas que se hacen cuando el programa ya está teóricamente correcto, a continuación de las Alfa.  

  - *De aceptación*  
El cliente da validez al programa.  
  
- **No Funcionales**    
Se comprueban temas adicionales como el rendimiento y la seguridad al margen de su aspecto funcional.  
  
  - *De usabilidad*  
Realizadas por los usuarios mismos que proporcionan información directa de la forma en la que el programa es usado realmente.  

  - *De rendimiento*  
Se comprueba lo rápido que efectúa sus tareas el programa en las condiciones reales de trabajo.  

  - *De stress*  
Se mide el rendimiento sometiendo el programa a las condiciones más extremas posibles. Por ejemplo poniendole una base de datos que ocupa el máximo de espacio posible, etc.  
  
  - *De seguridad*  
Se verifica la seguridad del programa haciendo pruebas de acceso, comprobando que son respetadas las partes que necesitan de autorización.  
  
  - *De compatibilidad*  
Se compueba que la aplicación funciona correctamente en diferentes entornos, por ejemplo en diversos navegadores.  

  - *De portabilidad*  
Se comprueba que la aplicación funciona correctamente en otros sistemas o equipos. p.ej. si funciona igual en Linux o en Windows, o corriendo en Windows bajo un determinado modelo y marca del portátil, etc.
***
### Forma de las pruebas  
Las pruebas pueden hacerse de forma *dinámica* o *estática*:  
  
- **Dinámicas**  
  Cuando realizamos *pruebas dinámicas*, comprobamos nuevas entradas y salidas mientras **ejecutamos el programa**.
- **Estáticas**  
  Cuando realizamos *pruebas estáticas* estamos comprobando posibles errores revisando el código fuente **sin necesidad de ejecutarlo**.  
  
***  
### Estrategias de prueba  

  Para la realización de las pruebas, a grandes rasgos, podemos seguir dos estrategias o enfoques:  
  
- **Prueba de caja blanca**  
  Analizamos el código fuente línea a línea, a través de cada una de sus funciones pertinentes viendo como se comporta cada parte durante su ejecución. Se revisa la cobertura de flujo del programa, comprobando condiciones y bucles (comprobar todos los caminos).
- **Prueba de caja negra**  
  Analizando el sistema sin entrar en lo que hace interiormente el código función por función, directamente trabajando desde su interfaz. Por ejemplo si en un programa de una calculadora ponemos un 2, la operación suma y como segundo operando le pasamos un 4, se espera un resultado por pantalla de 6.
  
![png caja blanca vs caja negra](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/caja_blanca-caja_negra.png)
  
Resumiendo, en las **pruebas de caja blanca** se comprueba la estructura examinando el código fuente de forma detallada, mientras que cuando se realizan las **pruebas de caja negra** sólo se comprueba la funcionalidad de la aplicación sin examinar su código de programación interno sino que se hacen pruebas desde afuera, comprobando entradas y salidas directamente desde su interfaz de usuario.

### Mecanismos de prueba
  
- **Automático**  
  Se usa software que realiza las pruebas de forma automatizada usando scripts desarrollados para hacer las comprobaciones.
- **Manual**  
  Las pruebas las realiza personal especializado en la tarea que desempeña la aplicación ya sea de dentro o fuera de la empresa.
***
## Pruebas de integración  
Consiste en la comprobación en conjunto de toda la aplicación.
  
La mejor forma de aplicar una prueba de integración es ir probando los módulos que forman el programa poco a poco, integrando unos pocos módulos conforme se van probando correctos se van añadiendo otros pocos sin testar. De esta manera se facilita la detección de errores. 
  
Aunque pueden haber enfoques en los que se integran todos los módulos de una vez (como sucede con el método del *Big bang*).
  
### Formas de integración:  
  
- **Big bang**  
Se integran todos los módulos juntos para que de lugar la "explosión" de bugs y errores (de ahí lo del "Big bang"). Con ello se reduce la cantidad de pruebas, pero se aumenta la dificultad de detectar la procedencia de los errores. Se trata de un método no incremental.

- **Ascendente**  
La construcción y la prueba se han realizado desde los niveles más bajos de la estructura del programa.
![jpg integracion ascendente](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/integracion-ascendente.jpeg)
- **Descendente**  
Se integran los módulos cayendo de arriba hacia abajo comenzando por el módulo de control principal.
![jpg integracion descendente](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/integracion-descendente.jpeg)
- **Continua**  
Se hacen pruebas automáticas de integración lo más a menudo que se pueda, continuamente durante todo el proceso de desarrollo del software.
*Jenkins*, *Bamboo* y *Travis CI*, son tres ejemplos de servidores web que permiten hacer pruebas de integración continua.

### Cobertura del código  
Cuando se hacen las pruebas, se usa este término para hacer referencia a la cantidad de código que se ha ejecutado/testeado referida en forma de porcentaje, siendo 100% en el caso en que se haya comprobado todo el programa. Ésto se puede hacer tanto desde el IDE como desde un servicio web.
***
![jpg calidad](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/calidad.jpeg) 
# Calidad  
  
Las pruebas que les hacemos a los programas tienen la finalidad de que estos lleguen al cliente con la calidad adecuada. 
En general, que un producto sea de calidad, quiere decir que cumple perfectamente con los requisitos para los que fue diseñado.

Para asegurar que nuestro producto salga con calidad se debe controlar esto durante el proceso de desarrollo.
Se puede verificar que los procesos que aseguran la calidad funcionan correctamente o que el producto en si funciona correctamente según la calidad que se espera de él.
A raiz de esto, existen dos conceptos a tener en cuenta:

- **QA**  
  Significa “*Quality Assurance*” (garantía de calidad). Garantiza la calidad en los procesos de creación/desarrollo.

- **QC**  
  Significa “*Quality Control*” (control de calidad). Garantiza la calidad de los productos desarrollados.  
  
Ambos departamentos trabajan en conjunto. La diferencia fundamental entre *QA* y *QC* es que mientras que el departamento de *QA* está presente desde la fase de diseño del producto, el departamento de *QC* comienza a trabajar cuando el producto ya está finalizado.  
  
## Factores de calidad  
Son los factores que contribuyen a que el producto desarrollado alcance la calidad deseada. Según el modelo más conocido (modelo de McCall):
![jpg diagrama modelo de McCall](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF2_1/main/mccall-grafico.jpeg)
  
 - ***Revisión***  
   -**Facilidad de Mantenimiento**  
  El código se ha de desarrollar de manera que sea sencillo de corregir. La mejor manera es hacer que las funcionalidades sean escritas en módulos, de manera que cuando algo no funciona podamos ir fácilmente a la sección que sospechamos que falla para arreglarla.  
  -**Facilidad de Prueba**  
Aquí se trata de asegurar que podremos probar cualquier cosa de forma sencilla. ¿Tenemos todas las herramientas necesarias al alcance para facilitarnos futuras pruebas?
  -**Flexibilidad**  
El código no debería ser rígido y debería facilitar las modificaciones futuras para facilitar la adaptación a cualquier cambio o nuevas necesidades.   
  
- ***Transición***  
  - **Interoperabilidad**  
Aquí lo que se pretende es si nuestro código funcionará correctamente en otro sistema o no.
  - **Portabilidad**  
Parecido a la anterior, pero desde el punto de vista del hardware o dispositivo que hará correr nuestro software.
  - **Reusabilidad**  
Este factor lo que busca es hacer que la mayor parte del código que escribimos pueda ser usado por otros códigos que escribamos.
- ***Operación***  
  - **Corrección**  
Nuestra aplicación debe hacer lo que se pretende.
  - **Fiabilidad**
El programa debe hacer lo que se pretende, y debe hacerlo siempre.
  - **Eficiencia**
La aplicación debería ejecutarse en los dispositivos para los que ha sido desarrollada de forma fluida y lo más rápidamente posible.
  - **Integridad**
Nuestra aplicación debería asegurar que los datos que maneja sean seguros, no se pierdan definitivamente ante cualquier fallo imprevisto, como un corte eléctrico, por ejemplo, asegurando copias de seguridad o mediante cualquier otro método. Además se deben controlar los accesos a datos, o partes del programa con acceso restringido.
 - **Facilidad de uso**
  Nuestra aplicación debe ser fácil o intuitiva a la hora de usarla de tal manera que puedan ejecutarse fácilmente todas sus funcionalidades.
