
| Identificador | ¿Qué imprimirá la consola? <br> (Predicción) | Justificación Teórica (Usa términos como: Hoisting, Ámbito de bloque, Ámbito de función, Undefined,...) |
| :--- | :--- | :--- |
| **Log A** | Imprime: Undefined|Esto pasa por el hoisting de var. JavaScript sabe que la variable producto existe porque la declaración se hace antes de empezar a ejecutar el código, pero todavía no le ha dado el valor "Teclado Mecánico", por eso su valor es undefined. |
| **Log B** | Imprime: Teclado Mecánico |Aquí ya se ha ejecutado la línea var producto = "Teclado Mecánico", por lo que la variable ya tiene ese valor y lo imprime. Como producto está declarada fuera de una función tiene ámbito global. |
| **Log C** |Imprime: 25 |Dentro del if se crea otra variable llamada descuento que usa let. Como let tiene ámbito de bloque, dentro de ese bloque se utiliza esta variable, que tiene el valor 25, |
| **Log D** |Imprime: 10 |Cuando salimos del bloque del if, la variable descuento creada con let ya no está disponible, entonces se utiliza la variable descuento que está declarada con var dentro de la función, cuyo valor es 10. var tiene ámbito de función.|
| **Log E** |Imprime: ¡ERROR CATÁSTROFICO!| La variable impuesto está declarada con const dentro del bloque del if, como const tiene ámbito de bloque, no podemos utilizarla fuera de ese bloque. Al intentar acceder a ella se produce un error, que es recogido por el catch.|
| **Log F** |Imprime: ¡ERROR CATÁSTROFICO!| precio está declarada con let y como let tiene ámbito de bloque, no se puede acceder a ella antes de que se ejecute su declaración. Por eso se produce un error y el catch muestra el mensaje de error. |
