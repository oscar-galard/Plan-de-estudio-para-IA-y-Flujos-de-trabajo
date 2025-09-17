# Resumen de la Evolución de los Modelos de Lenguaje

## ELIZA (1966)
Fue el primer "chatbot", un programa que simulaba una conversación. No entendía el lenguaje, sino que usaba un conjunto de reglas básicas y palabras clave para reflejar las frases del usuario. Su ingenio demostró que una computadora podía engañar a los humanos para que creyeran que estaban conversando con una inteligencia real.

### El Contexto de 1966
En 1966, no existían las computadoras personales, ni los monitores como los conocemos hoy. Las computadoras eran gigantescos sistemas llamados mainframes que ocupaban habitaciones enteras y eran compartidos por toda una institución.

La forma de interactuar con ellas no era con un teclado y un ratón, sino a través de un teletipo (TTY). Piensa en un teletipo como una máquina de escribir muy grande que estaba conectada a la computadora con cables.

- Tú escribías una línea de texto en el teletipo y pulsabas "enter".
- La máquina enviaba ese texto al mainframe, que lo procesaba.
- La respuesta del programa se imprimía en un rollo de papel en el teletipo.
- Así que sí, no había pantallas; todo era texto impreso en papel.

### ¿Qué era ELIZA Realmente?
ELIZA no era un programa de inteligencia artificial en el sentido moderno de la palabra. Era un programa de procesamiento de lenguaje natural muy rudimentario que simulaba ser un psicoterapeuta.

Su creador, Joseph Weizenbaum, se basó en la terapia rogeriana, un tipo de terapia que se centra en reflejar lo que dice el paciente para animarlo a hablar más. ELIZA no tenía ninguna comprensión real del lenguaje, solo usaba un conjunto de reglas muy básicas y predefinidas.

### ¿Cómo Funcionaba?
El funcionamiento de ELIZA era increíblemente simple, lo que lo hacía tan ingenioso. El programa buscaba palabras clave y patrones en lo que escribías y luego aplicaba una regla para generar una respuesta.

Tomemos el ejemplo:
- Tú escribes: "I feel sad." (Me siento triste.)
- ELIZA analiza tu frase: Busca una palabra clave. Encuentra el patrón "I feel" (me siento).
- ELIZA aplica una regla: La regla para el patrón "I feel" es transformar la frase en una pregunta que la refleje.
- ELIZA genera la respuesta: Cambia "I feel" por "Why do you feel" (por qué te sientes) y el adjetivo "sad" (triste) lo deja tal cual.
- ELIZA imprime la respuesta: "Why do you feel sad?" (¿Por qué te sientes triste?).
- Si no encontraba ninguna palabra clave, tenía una respuesta genérica como "¿Puedes elaborar más sobre ese tema?".

El genio de ELIZA fue que, a pesar de no entender nada, era tan convincente que las personas se enganchaban emocionalmente a la conversación. Fue la primera vez que un programa demostró que una simulación exitosa de la conversación era posible, abriendo el camino para todo lo que vino después.

## PLN Simbólico (Años 80s-90s)
Este enfoque, a diferencia de ELIZA, sí intentaba que las computadoras "entendieran" el lenguaje, pero lo hacían de una manera muy rígida: a través de reglas y lógica humana codificadas a mano.

Imaginemos a un programador escribiendo miles de reglas como:

1. Si la oración empieza con una pregunta ("¿Qué", "¿Por qué", etc.), la respuesta debe ser una oración declarativa.

2. Si un sustantivo es seguido por un verbo, el verbo debe concordar con el género y número.

3. "Sintaxis" es más importante que "sentido".

El problema: Este método era increíblemente frágil. Funcionaba bien para oraciones muy simples, pero se rompía ante la ambigüedad, los errores gramaticales o el lenguaje figurado. Era como un robot bibliotecario: sabía todas las reglas, pero no entendía una metáfora.

Por ejemplo, si un humano le decía "El tiempo vuela como una flecha", un sistema de PNL simbólico no podría entender que "vuela" es un verbo figurado. Podría confundirse y buscar la palabra "flecha" en un diccionario.

## PLN Estadístico (1998)
Marcó el gran cambio hacia los datos. Los modelos dejaron de usar reglas y comenzaron a aprender de enormes cantidades de texto. A través de conceptos como los n-gramas, aprendían la probabilidad de que una palabra siguiera a otra, lo que les permitía generar texto de forma más fluida.

Aquí es donde la computación dio un salto de fe. En lugar de darle reglas a la computadora, los investigadores le dieron una enorme cantidad de texto (libros, artículos, etc.) y le dijeron: "Aprende tú mismo las reglas analizando la frecuencia de las palabras".

El concepto clave aquí son los n-gramas. Un n-grama es una secuencia de "n" palabras. Por ejemplo, en la frase "Quiero ir a casa", los 2-gramas son: "Quiero ir", "ir a", "a casa".

### ¿Cómo funciona? El modelo no entiende la gramática, pero sí la probabilidad.

El modelo de n-gramas "lee" millones de textos y aprende que, después de "quiero ir a", las palabras que siguen con mayor probabilidad son "casa" (70%), "la tienda" (20%), "la playa" (5%), etc.

Cuando tú le dices "Quiero ir a...", el modelo calcula la probabilidad de la siguiente palabra basándose en lo que ha visto antes, y elige la más probable.

Este enfoque era mucho más flexible que el simbólico. Aunque el modelo no "entendía" el lenguaje, podía predecir la siguiente palabra de forma sorprendentemente precisa basándose en patrones estadísticos, lo que le permitía manejar el lenguaje natural de una forma más fluida. Fue el primer paso hacia los modelos de lenguaje modernos.

## Word Embeddings (2013)
Esta innovación convirtió las palabras en vectores de números en un espacio multidimensional. Esto permitió que las computadoras entendieran las relaciones y la semántica (el significado) entre las palabras, haciendo posible realizar operaciones matemáticas como "Rey - Hombre + Mujer = Reina".

Este fue un salto enorme, un cambio de chip en la forma de pensar sobre el lenguaje. Dejó de ver las palabras como simples etiquetas o secuencias, y las convirtió en vectores de números en un espacio multidimensional.

Imagina que cada palabra es un punto en un mapa. Los puntos que están cerca unos de otros tienen un significado similar. Por ejemplo, la palabra "gato" está cerca de "perro" y "mascota", pero muy lejos de "televisión" o "coche".

Lo más asombroso de esto es que, una vez que las palabras se convierten en números, la computadora puede hacer matemáticas con ellas. El famoso ejemplo es:

- Rey - Hombre + Mujer = Reina

La computadora encuentra el vector para "Rey", le resta la "dirección" del vector "Hombre" y le suma la "dirección" del vector "Mujer". El resultado es un nuevo punto en el mapa que está increíblemente cerca del vector de la palabra "Reina". Esto le dio a la IA, por primera vez, una forma de entender la semántica (el significado de las palabras) más allá de su simple frecuencia.

## Transformers (2018)
Una arquitectura revolucionaria que introdujo el mecanismo de atención, permitiendo que los modelos procesaran todas las palabras de una oración al mismo tiempo. Esto resolvió el problema del contexto en frases largas y es la base de todos los modelos de lenguaje masivos.

Si los Word Embeddings le dieron a la IA un mapa, los Transformers le dieron la habilidad de navegarlo de forma inteligente. Esta arquitectura, creada por Google, fue el punto de inflexión que hizo posible a los modelos de lenguaje masivos.

Antes de los Transformers, los modelos leían las frases como si fueran un libro: palabra por palabra, de forma secuencial. Al final de una oración larga, el modelo ya se había "olvidado" de las primeras palabras, perdiendo el contexto.

La idea revolucionaria del Transformer es lo que se conoce como "mecanismo de atención". En lugar de leer secuencialmente, el modelo puede "mirar" todas las palabras de una oración al mismo tiempo y entender cómo se relacionan entre sí.

Por ejemplo, en la oración: "El niño le lanzó la pelota al perro y éste la atrapó."

Un modelo antiguo podría tener problemas para saber si "éste" se refiere al niño o al perro. Un Transformer, sin embargo, puede "prestar atención" a las palabras clave "niño", "pelota" y "perro" al mismo tiempo y determinar, por contexto, que "éste" se refiere al perro.

Esta capacidad de entender el contexto completo de una oración de una sola vez es lo que desbloqueó el potencial para crear modelos gigantes como BERT y GPT, y es la base de la mayoría de los modelos de IA que usamos hoy.

## BERT (2018)
Un modelo basado en Transformers que se especializó en la comprensión bidireccional. Podía entender el contexto de una palabra analizando tanto lo que venía antes como lo que venía después, lo que lo hizo muy efectivo para tareas de búsqueda, preguntas y respuestas.

Si el Transformer le dio a la IA la capacidad de "prestar atención" a toda una oración, BERT llevó esta idea un paso más allá. BERT fue entrenado para entender el contexto de una palabra mirando las palabras a su izquierda y a su derecha al mismo tiempo.

Piensa en una frase como: "El banco del río es de arena."

Un modelo de lenguaje antiguo vería "El banco del..." y podría adivinar "banco" como una institución financiera. BERT, sin embargo, ve la palabra "río" al mismo tiempo y sabe que "banco" se refiere a la orilla, no a una entidad financiera.

Esta capacidad de entender el contexto completo de una palabra le dio a BERT una gran precisión en tareas como responder preguntas, clasificar textos (por ejemplo, si una reseña es positiva o negativa) y mejorar los resultados de búsqueda.

## GPT-3 (2020)
La primera demostración a gran escala del potencial de la arquitectura Transformer. Con 175 mil millones de parámetros, podía generar contenido creativo y coherente como código, ensayos y correos electrónicos, marcando la diferencia entre los modelos que comprenden y los que crean.

El éxito de GPT-3 no se debió a una nueva arquitectura radical, sino a la escala. Utilizó la misma arquitectura de Transformer, pero fue entrenado con una cantidad de datos y una cantidad de parámetros (175 mil millones) nunca antes vista.

Este tamaño masivo le permitió aprender patrones tan complejos que podía generar texto coherente y creativo, no solo predecir la siguiente palabra. Si el PNL estadístico podía predecir la siguiente palabra en una frase, GPT-3 podía escribir un ensayo, una poesía o código completo con una simple indicación.

Fue el primer modelo que, para la mayoría de las personas, se sintió como una conversación con un asistente de verdad, capaz de entender la intención y responder de forma creativa y fluida.

## GPT-4 (2023)
Una evolución que agregó multimodalidad (la capacidad de procesar texto e imágenes) y un razonamiento mejorado. Es un modelo más versátil y capaz que puede resolver problemas complejos y seguir instrucciones más detalladas.

GPT-4 es una evolución de GPT-3 que se distingue principalmente por dos cosas: su capacidad multimodal y su razonamiento mejorado.

Multimodalidad: A diferencia de GPT-3, que solo trabajaba con texto, GPT-4 puede entender y procesar diferentes tipos de datos, como imágenes y texto, al mismo tiempo. Por ejemplo, podrías subir una foto de una gráfica y pedirle que te explique lo que muestra.

Razonamiento y Creatividad: Es significativamente más inteligente, capaz de resolver problemas complejos, entender matices, y seguir instrucciones más detalladas y creativas. GPT-4 es el modelo que llevó la IA a aplicaciones más sofisticadas como la educación, el análisis de documentos legales y la programación asistida, demostrando una capacidad de "razonar" que va más allá de la simple generación de texto.

https://es.wikipedia.org/wiki/ELIZA
historia eliza
https://www.bbc.com/mundo/noticias-44290222

https://www.tokioschool.com/noticias/que-es-procesamiento-lenguaje-natural/

https://www-dataversity-net.translate.goog/a-brief-history-of-natural-language-processing-nlp/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

https://es.wikipedia.org/wiki/Word_embedding

https://en.wikipedia.org/wiki/Transformer_(deep_learning_architecture)

https://es.wikipedia.org/wiki/BERT_(modelo_de_lenguaje)

https://es.wikipedia.org/wiki/GPT-3
