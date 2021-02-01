## M5-UF2-1 Optimitzación del Software
![logos de varis S.O.](https://raw.githubusercontent.com/jesus-zafra/Apuntes_UF1_1/main/so-icons.jpg)
### Pruebas de software  
Consiste en probar que nuestros programas funcionan como deberían para conseguir que sea un software de calidad, o lo que es lo mismo, conseguir que desempeñen todo aquello que se pedía en sus especificaciones o requisitos descritos durante su fase de diseño de la mejor forma posible. Para ello se comprueban diferentes resultados dando al programa diferentes entradas y observando que los resultados son los esperados.  
### Frameworks
Para facilitar el desarollo de las pruebas podemos usar *Frameworks*. Éstos son un entorno de desarrollo de software que unifica una serie de criterios, librerías y recursos de cara a programar de una forma estandarizada de forma que siguiendo esas pautas nos veamos todos obligados a utilizar buenas prácticas de programación y facilitan enormemente la comprensión del código entre todos los miembros participantes en un equipo de programación.  

En general, un *Framework* se compone de:
- **Reglas** o partes que obligan al cumplimiento de *buenas prácticas de programación*
- **Herramientas comunes**
- **Bibliotecas**

### Tipos de pruebas
- **Funcionales**  
Sirven  para comprobar que todo funciona tal como se especificó en su diseño en base a los requisitos, o especificaciones iniciales.
- **No Funcionales**  
Se comprueban temas adicionales como el rendimiento y la seguridad al margen de su aspecto funcional.

- **Pruebas dinámicas**  
  Comprobamos nuevas entradas y salidas mientras vamos ejecutando el programa.
- **Pruebas estáticas**  
  Comprobamos posibles errores revisando el código fuente sin necesidad de que lo tengamos que ejecutar.   
  
Para realizar las pruebas existen dos tipos de estrategia:  

- **De caja negra**  
  Analizando el sistema sin entrar en lo que hace interiormente el código función por función, directamente trabajando desde su interfaz. Por ejemplo si en un programa de una calculadora ponemos un 2, la operación suma y como segundo operando le pasamos un 4, se espera un resultado por pantalla de 6.
- **De caja blanca**  
  Analizamos el código fuente línea a línea, a través de cada una de sus funciones pertinentes viendo como se comporta cada parte durante su ejecución.
