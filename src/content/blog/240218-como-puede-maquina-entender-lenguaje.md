---
title: '¿Cómo puede una máquina entender el lenguaje humano?'
description: 'Los embeddings son la base de los actuales modelos de Procesamiento de Lenguaje Natural, es decir, los que permiten que la Inteligencia Artificial sea capaz de procesar el lenguaje humano para resumir textos, crear sistemas de recomendación, búsquedas semánticas, traductores o clasificadores.'
pubDate: "2024-02-18T14:47:36.441Z"
heroImage: '/dialogo-hombre-maquina.jpg'
categories: ['NLP']
tags: ['Embeddings', 'Corpus', 'Lenguaje']
author: '["Oscar Pérez-Lora"]'
---

Hace muy poco, parecía que el lenguaje era una característica propia de los seres humanos y que ello nos atribuía cierto carácter único y especial, a veces superior frente a otros seres de la naturaleza. Ahora, las máquinas lo pueden hacer igual o mejor que nosotros. ¿Realmente lo hacen como nosotros o simulan hacerlo? El concepto de los embeddings es la clave para responder a esta pregunta.

Los embeddings son una representación numérica de la información contenida en determinados medios, como audio, video o texto. Dicha representación numérica permite que nuestro computador "entienda" la información que le hemos introducido. Es decir, en lugar de procesar imágenes, sonidos o palabras como tales, la computadora procesa y calcula un conjunto de números. En resumen, entender para la computadora significa procesar y calcular números.

Pero, ¿cómo es posible convertir palabras en números? Justamente en esto consisten los embeddings: llevar las sentencias a un espacio vectorial. Pero primero debemos entender qué es un vector como unidad fundamental de un espacio vectorial.

Supongamos que queremos visitar el nuevo departamento de un amigo. Sabemos que el departamento se encuentra en la ciudad en la que vivimos, pero requerimos indicaciones precisas para poder llegar a ese departamento en concreto y no a cualquiera de los miles que se encuentran en la ciudad. Es decir, la ciudad es un espacio que contiene miles de departamentos. Identificar el departamento de nuestro amigo dentro del espacio requiere de una dirección: número de la calle, número de la carrera y número del departamento. Por ejemplo, calle 15 con carrera 8, apartamento 703.

La dirección es un vector, es decir, un conjunto de números que nos permiten ubicarnos dentro de la ciudad (espacio). En nuestro ejemplo, dichos números son [15, 8, 703]. Podemos ahora asignar a cada uno de los departamentos un vector único (dirección) que nos permita ubicarlos dentro de la ciudad. Podemos deducir, por ejemplo, que el vector [15, 8, 702] es vecino del departamento de nuestro amigo, en términos de cercanía en el espacio.

Esto que realizamos con la dirección de nuestro amigo en el espacio de la ciudad, es similar a lo que hacen los embeddings con las palabras dentro de un texto. Es decir, las palabras o las frases no son entidades sueltas o arbitrarias; por el contrario, existe una serie de relaciones semánticas dentro de un texto. Si pensamos en la palabra "perro", podemos asociarla con otras palabras o expresiones como "cuatro patas", "mamífero", "pelota", "parque", "mascota", etc. Son palabras vecinas. De igual manera, hay otras palabras que se encuentran lejos de "perro", como "avión", "París" o "Marte". Ahora bien, sería posible encontrar una frase como "en París, los perros peligrosos deben llevar un bozal". En este caso, dicha posibilidad es menos frecuente (o menos probable) que "el perro es una mascota ideal para los niños". Es decir, en el espacio del corpus que representa un texto o conjunto de textos, las palabras y las frases ocupan determinadas posiciones semánticas que las relacionan entre sí.

Existen muchas maneras de constituir dicho espacio semántico (casi como si dijéramos que existen muchas maneras de organizar los departamentos dentro de una ciudad). Se entiende por modelo de lenguaje la manera de construir el espacio vectorial, que no es otra cosa que la posición semántica entre palabras o frases. Por esto mismo, hay muchos modelos de lenguaje y de manera permanente se sigue investigando en este campo. Al momento de introducir un requerimiento a un modelo de lenguaje, como puede ser en ChatGPT, el modelo de lenguaje toma nuestro texto, lo convierte en vectores, lo lleva a dicho espacio vectorial y, de acuerdo con su "dirección", lo ubica en determinado vecindario semántico. La respuesta que posteriormente nos ofrece el modelo de lenguaje depende de la cercanía con el texto que hemos introducido

Determinados modelos de lenguaje cumplen tareas específicas en relación con el lenguaje. Entre las más comunes se encuentran:

1. *Resumen de textos*: a partir de ingresar un texto largo el modelo mantiene un valor semántico similar pero con un número menor de frases.
2. *Sistemas de recomendación*: si introducimos una serie de condiciones o de preferencias, el modelo de lenguaje ubica en el espacio vectorial aquello que más se ajusta a dichas condiciones. Un ejemplo muy común sería un sistema de recomendación de películas, en donde le podemos indicar que queremos ver algo de comedia y ciencia ficción, con una valoración alta y que haya sido taquillera. Entre la respuesta obtendremos seguramente películas como *Volver al Futuro*.
3. *Búsqueda semántica": relaciona una frase o texto que introduzcamos al modelo de lenguaje con otras frases o textos que estén presentes en el espacio vectorial. Por ejemplo, si deseo buscar en el *corpus* algo que hable de los efectos secundarios de una determinada vacuna, el modelo regresa una frase que sea semánticamente cercana a nuestro texto. Es útil si tenemos una idea vaga de algo y que nos permite encontrar específcamente lo que buscamos.
4. *Traductores*: en este caso el modelo relaciona un texto en un idioma y su cercanía semántica en otro idioma. Por ejemplo, al introducir "casa" el modelo encuentra similitud semántica con las palabras "home" o "house" (dependiendo del contexto de la frase eligirá una u otra acepción).
5. *Clasificadores*: el modelo de lenguaje bien puede tomar un *corpus* e identificar diversas temáticas al interior del mismo.

Los modelos de lenguaje natural permiten a las computadoras procesar los textos y ofrecer diversas salidas. Ahora bien, es claro que la computadora no entiende el lenguaje en el sentido que nosotros lo hacemos. El ser humano usa el lenguaje en tanto intencionalidad: expresa deseos y estados del mundo. Las máquinas carecen de deseo y de comprender estados del mundo. Si tenemos hambre y vamos a un restaurante usamos el lenguaje con la intención de realizar un cambio en el estado del mundo; pasar de tener hambre a otro estado del mundo en el que hemos saciado nuestro apetito. Le solicitamos al camarero lo que deseamos comer. Una máquina simplemente procesa y calcula números.

No obstante, no deja de ser interesante que si bien los cálculos que realiza la máquina y nuestros procesos cognitivos son completamente diferentes, pero llegan a un resultado más o menos similar. Esto sucede porque los modelos han sido entrenados con nuestras propias interacciones con el lenguaje, y simplemente identifica cuáles deberían ser los valores más probables de ocurrencia.

