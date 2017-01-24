Guia de estilo John Papa ANGULAR 2
https://angular.io/docs/ts/latest/guide/style-guide.html

Guia de estilo John Papa ANGULARJS
https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md 

Google Web Component
https://github.com/GoogleWebComponents/style-guide 

Polymer
https://polymerelements.github.io/style-guide/#documentation 

Guia de estilo Javascript
https://github.com/airbnb/javascript

Recomendaciones estilos CSS
https://github.com/airbnb/css 
slides de charla de Francisco Quintero, miembro del equipo de Serenity FrontStack
http://slides.com/frontstack/deck-4#/ 

PRINCIPIOS CLEAN CODE

Principio DRY (Don't repeat yourself)
No repitas código NUNCA, El código duplicado es propenso a generar errores y es difícil de mantener. Si estás repitiendo código, extrae ese código a una función para encapsularlo. Si tenemos que hacer un cambio, este estará localizado en un solo punto, y no desperdigado por todo el código fuente.
The Principle of Least Surprise.
las funciones o clases deben hacer lo que (razonablemente) se espera de ellas. Es decir, una función o una clase debe tener, en función de su nombre, un comportamiento obvio para cualquier programador, sin que este tenga la necesidad de sumergirse en su código.
Principio KISS (Keep It Simple Stupid)
El diseño de un programa debe ser sencillo. Cuánto más sencillo sea, mejor. Hay que evitar la complejidad como norma general, pero sobre todo la complejidad innecesaria.

Principio SOLID
realmente son 5 principios
SRP  (Single Responsibility Principle, las clases o módulos deben tener una única responsabilidad
Open/Close Principle, Abierto para su extensión, pero cerrado para su modificación. nos dice que el código está mejor diseñado si se puede modificar su comportamiento sin cambiar su código fuente. Debería bastar con añadir código, en lugar de modificarlo. No deberíamos necesitar modificar una clase a no ser que sea para corregir errores.
Liskov, principio de sustitución, una clase derivada no debe modificar el comportamiento de la clase base.
ISP Interface segregation principle) una clase que implementa una interfaz no debe depender de métodos que no utiliza. Esto como norma general implica que nuestras interfaces deben ser sencillas y tener pocos métodos. Es preferible tener varias interfaces pequeñas, a tener una interfaz grande. Así no obligamos a los clientes a depender de métodos que no necesitan implementar.

DIP Dependency Inversion Principle), que viene a decir que las clases de alto nivel, no deben depender de clases de bajo nivel. Ambos deben depender de abstracciones. Además las abstracciones no deben depender de los detalles, si no que los detalles deben depender de las abstracciones. En definitiva, lo que tenemos que hacer es invertir las dependencias.

Principio SoC, 
(separation of concerns) Los asuntos, son los diferentes aspectos de la funcionalidad de nuestra aplicación. Por ejemplo la capa de negocio, la capa de datos etc. Un buen ejemplo de separación es el patrón MVC.

Principio YAGNI, (You ain't gonna need it), viene a decir que no debemos implementar algo si no estamos seguros de necesitarlo. Así ahorramos tiempo y esfuerzo.

Principio Boy Scout El código siempre puede mejorar. Si podemos, debemos refactorizar el código para dejarlo todavía más limpio y simple que antes.

Ley de Demeter, una unidad solo debe tener conocimiento limitado de otras unidades, y solo conocer aquellas que están relacionadas. La una unidad solo debe hablar con amigos y nunca con extraños. Además la unidad solo debe hablar con amigos inmediatos.no hay que hablar con extraños.

F.I.R.S.T.
Los test forman un papel fundamental en el arte de escribir código limpio. No obstante, no es suficiente con escribirlos de cualquier manera. Deben cumplir una serie de reglas.
Fast: los test deben correr rápido. Deben tardar poco en ejecutarse. De no ser así, es probable que nos de pereza ejecutarlos y, por tanto, que no lo hagamos con la frecuencia deseada. El no ejecutar los test con relativa frecuencia puede hacer que tardemos más en encontrar los problemas que vayan surgiendo.
Independent: los test deben ser independientes unos de otros. El resultado de un test no debe condicionar el de los siguientes. Deben poder ejecutarse en el orden que se quiera. De lo contrario, un fallo en el primer test, puede desencadenar un fallo en cascada de los demás, haciendo complejo el diagnóstico del sistema.
Repeatable: los test deben poder ejecutarse en cualquier entorno (desarrollo, pre-producción, producción…). De no ser así, siempre tendremos una excusa para cuando los test fallen.
Self-Validating: los test deben devolver una respuesta booleana. Pasan o no pasan. No deben dejar una cadena de caracteres en un fichero de log que tengamos que comprobar nosotros mismos, o dejar dos ficheros de un tamaño determinado que, igualmente tengamos que comprobar. De lo contrario, requerirán una alta evaluación manual que nos hará perder tiempo y precisión.
Timely: los test deben ser escritos antes que el código de producción. De no ser así, el código de producción será difícil de testear.

Resumen clean Code interesante
http://samuelcasanova.com/2016/09/resumen-clean-code/

Herramientas trabajo
para angular2, VISUAL STUDIO CODE
https://code.visualstudio.com/
aunque tambien se puede usar otro editor añadiendo el plugin para TypeScript
para el resto de frameworks,  con el que el desarrollador se sienta más cómodo, (Visual Studio Code, SublimeText, Atom, WebStorm, etc)
recomendamos instalar un plugin de ESLINT, el que corresponda con cada editor, para que muestre en tiempo real errores de estilo de código


Progressive Web Application
https://github.com/GoogleChrome/lighthouse
Auditing, performance metrics, and best practices for Progressive Web Apps


