# Memory-game-kata
Kata de Javascript intermedio para el 1er evento Marzo Node Girls Madrid  💪 💪

### ¿Qué construirás?
El Juego de la Memoria es el clásico juego de buscar las parejas de cartas idénticas, algo a lo que también se le ha llamado el Juego de la Concentración. A este te proponemos añadirle más funcionalidades como un panel de resultados (score), un botón de *empezar de nuevo* y un cronómetro. Ah!! Y sin olvidarnos la ventana de **Has ganado el juego!!**

El estilo lo puedes replicar para centrarte en desarrollar el dinamismo del juego con Javascript, o modificarlo o hacerlo desde cero! Tú decides!


### Cómo funciona el juego
El tablero consiste en 16 cartas colocadas en un *grid* o cuadrícula de 4x4. Son 8 parejas de cartas, cada una con su símbolo característico. Las cartas están dispuestas de manera **aleatoria** con el símbolo hacia abajo. 

La dinámica es sencilla: la jugadora al clicar una carta la da la vuelta y tiene que localizar la que es igual a la que acaba de salir.

En cada turno:
- La jugadora da la vuelta a una carta para revelar el símbolo que contiene
- Se da la vuelta a una segunda carta, tratando de encontrar su pareja igual correspondiente
- Si las cartas coinciden, se quedan dadas la vuelta
- Si no coinciden, ambas se quedan boca abajo
- El juego termina cuando has acertado todas las parejas!! 🌟🌟 

#### Funcionalidades que tener en cuenta
Tenéis que recrear los efectos de las interacciones en estos casos:
- Cuando las cartas coinciden
- Cuando las cartas no coinciden
- Cuando el juego termina

### Código y esqueleto para empezar
Por supuesto que puedes empezar desde 0 y utilizar Boostrap o CSS nativo. Aún así, queremos que aproveches mejor el tiempo de los katas saltándo directamente al Javascript. Será un reto interesante también si tu tarea es revisar el código de otra persona y en función de eso, montar tu archivo de Javascript para las funcionalidades y hacerlo funcionar!

### Estrategia de desarrollo
Te recomendamos planificarte y hacerte issues para seguir convenientemente esta estrategia de desarrollo que te recomendamos.
Monta tu proyecto en pequeñas piezas y trabaja en ramas (Git/GitFlow) como ya sabes 😜. 

Para un mejor aprovechamiento del tiempo, te mostramos un ejemplo de estrategia de desarrollo, pero por supuesto puedes hacerlo como desees. Allá vamos:

**1.  Comienza por construir la cuadrícula o grid de cartas. El resto de la funcionalidad del juego, depende de ella.**

Cada vez que la jugadora clica el botón *restart* las cartas deberían colocarse de manera aleatoria cada vez o *randomly*.

**2. Añade la funcionalidad que gestiona los clicks.**

Cada click debe revelar el lado "oculto" de cada carta. El click en la primera carta la dará la vuelta, enseñará el símbolo y quedará dada la vuelta. El segundo click a una carta diferente también la dará la vuelta y enseñará el símbolo.

Te recomendamos aquí usar **event delegation**. En vez de añadir un evento a cada carta, lo cual baja la performance de la aplicación, ¿recurdas alguna manera de añadirselo al *nodo padre*? Echa un vistazo al `index.html` para ver qué nodo puede ser.

**3. Trabaja ahora en la lógica de los aciertos** Llegadas a este punto, las jugadoras pueden dar la vuelta a las cartas. Ahora nos preguntamos: ¿"sabe" tu juego si la jugadora ha acertado o no?

Recomendaciones: 

- Piensa sobre cómo se pueden "almacenar" temporalmente las cartas abiertas, y que sean sólo 2 las que se comparan 
- Trata de limitar a la jugadora dar la vuelta a más de 2 cartas y prevenirla de seleccionar la misma carta 2 veces
- Si las 2 cartas coinciden, ¿cómo afecta a la clase o `class` de las cartas? Echa un vistazo al `index.html`
- Si la lógica de los aciertos se repite mucho, considera una refactorización del código

**4. Ahora crea la condición de juego ganado** ¿Cómo "sabe" tu juego que la jugadora ha ganado?

¡La jugadora deberá ver un modal que le indique que ha ganado! Pregúntate, ¿qué información deberá contener ese modal?

**5. Implementa funcionalildad adicional**

Te recomendamos en este punto añadir cosillas molonas, pero vamos, que ya tienes tu MVP!!! 🙌 🙌 

- Contador de movimientos que lleva la jugadora (nº de cartas volteadas)
- Cronómetro para medir el tiempo que lleva el juego activo. Se para cuando el juego se haya completado
- Contador de éxito o *star rating* mostrará según el nº de clicks que se hagan, cómo afecta a tener una calificación de 3 estrellas (de lo que partimos al inicio del juego) o menos, que se irán restando a medida que se cliqueen más cartas
- Botón de *reset* o *empezar de nuevo* que resetea toda la cuadrícula o *grid* de cartas
 

**Para el fork, los ejemplos y funcionalidades 👉 https://kooltheba.github.io/memory-game/ + https://github.com/udacity/fend-project-memory-game**


#### Nota y agradecimientos
Este es un proyecto propuesto por Udacity en uno de sus Nanodegrees. Agradecemos los contenidos y el mantenimiento del proyecto por parte de todos los contributors y mantainers.





















