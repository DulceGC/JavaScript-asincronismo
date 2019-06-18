# JavaScript-asincronismo

**Descripcion sencilla de como funciona el asincronismo en JS
** :smile:

Java Script no es multitarea, por lo que le manda a hacer la ejecucion a otros procesos a esto se le llama EventLoop.
JavaScript tiene algo llamado la pila de ejecucion o 'callstack' donde va poniendo las llamadas a las funciones segun el orden de ejecución de nuestro programa; si una función llama a otra, entonces esta se agrega a la pila.
Cuando termina de ejecutar una funcion la saca de esa pila y la desecha.
En algún momento dado nuestro programa necesita algún dato de otro sitio en la web y le pide al navegador que cuándo obtenga los datos ejecute cierta función.
Esta tarea que se lleva el navegador se llama 'callBack'
Mientras tanto JS sigue ejecutando nuestro programa principal y cuando la respuesta llega va a parar a la 'cola de tareas'.
Aqui las tareas se ordenan una detrás de la otra a medida de que van llegando.

*¿Que tareas van a parar a esta cola?*
- Las peticiones a servidores.
- Las interacciones visuales.
- Los eventos que se realizan cada cierto tiempo.

Recien cuando el programa se queda sin funciones en la pila de ejecucion es que va a ir a buscar las funciones en la cola de tareas por eso es que hay que tener cuidado de no generar cuellos de botella en la pila de ejecución. Si esto llegará a pasar JS tardaría mucho en ejecutar el programa.

conclusión:

**NO BLOQUEAR EL EVENTLOOP**
