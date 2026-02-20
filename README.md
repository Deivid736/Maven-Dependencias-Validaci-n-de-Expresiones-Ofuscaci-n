# Maven-Dependencias-Validaci-n-de-Expresiones-Ofuscaci-n

¿Qué tanto se dificulta la lectura?
La lectura del código ofuscado se vuelve bastante más complicada que la del código original. Los nombres de las clases y métodos ya no son claros, sino letras o nombres raros, entonces ya no puedes entender de un solo vistazo qué hace cada cosa. Para comprenderlo toca ir siguiendo el flujo del programa y probando mentalmente qué hace cada parte.

¿Se pierde claridad estructural?
Sí, se pierde bastante. Aunque el código sigue teniendo clases y métodos, todo se ve más desordenado porque los nombres ya no ayudan a entender la estructura del proyecto. Ya no es tan fácil identificar qué clase valida las expresiones, cuál maneja la pila o dónde empieza realmente la ejecución, así que ubicarse en el proyecto cuesta más.

¿Sigue siendo posible entender la lógica?
Sí, todavía se puede entender la lógica, pero toma más tiempo y esfuerzo. Viendo cómo se llaman los métodos, cómo se usan las variables y qué sale en consola, se puede deducir qué está haciendo el programa. O sea, no es imposible, solo es más cansado y menos directo que con el código sin ofuscar.

Conclusión breve confirmando que el comportamiento no cambió:
Después de ofuscar el proyecto, el programa sigue funcionando exactamente igual que antes. Las entradas producen las mismas salidas, la validación de expresiones devuelve los mismos resultados y no hubo cambios en el comportamiento desde consola. Lo único que cambió fue cómo se ve el código por dentro al decompilarlo; la lógica y el funcionamiento del programa se mantuvieron intactos.


instrucciones para compilar y ejecutar.
Primero abre la consola (cmd) y ubícate en la carpeta raíz del proyecto, donde se encuentra el archivo pom.xml. Luego compila el proyecto ejecutando el comando mvn clean package; este proceso limpia compilaciones anteriores y genera el archivo .jar dentro de la carpeta target.

Una vez que termine la compilación, puedes ejecutar la versión normal del programa usando el comando java -cp "target/stackHandler-0.0.1-SNAPSHOT.jar;target/libs/" stackHandler.handler.Main "(a+b)[c-d]". Si deseas ejecutar la versión ofuscada, utiliza el comando java -cp "target/stackHandler-0.0.1-SNAPSHOT-obf.jar;target/libs/" stackHandler.handler.Main "(a+b)[c-d]".

En ambos casos, la expresión que aparece entre comillas al final es la que se va a validar, y puedes cambiarla por cualquier otra para realizar diferentes pruebas. Con estos pasos puedes compilar y ejecutar correctamente tanto la versión original como la versión ofuscada del proyecto desde consola.
