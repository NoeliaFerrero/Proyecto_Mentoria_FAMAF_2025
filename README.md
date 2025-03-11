# Mentoria FAMAF 2025 

# Proyecto: ***El robo del Siglo ~ El plan secreto para predecir sitios fraudulentos***

<div align="center">

<p align="center">
  <img src="https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/bcc026f560f5e02d119e2826ca38789d5b0253b0/portadaV1__cleanup_cleanup.png">
</p>
</div>

# Tabla de contenidos 📖
- [Introduccion](#introduccion)
- [Contexto](#Contexto)
  - [Objetivo](#objetivo)
- [Contexto Analítico](#Contexto_Analítico)
  - [Diccionario de Datos](#diccionario_de_datos)
  - [Vista previa de los datos](#vista_previa_de_los_datos)
- [FAQs](#faqs)
  - [¿Qué te sumaría participar en este proyecto?](#faq1)
  - [Este proyecto es para vos si...](#faq2)

## Introduccion 

En 2006, un grupo de ladrones vació el Banco Río de Acassuso, Buenos Aires, sin disparar un solo tiro.

El saqueo quedó instalado en el imaginario social como El robo del siglo. Así lo bautizaron los medios cuando comenzaron a revelarse los detalles de un atraco tan meticuloso que parecía sacado de la mente de un guionista sofisticado: una toma de rehenes con armas de juguete, un túnel de 15 metros para trasladar el dinero, gomones, diques improvisados, la huida a través de las alcantarillas y un botín de 20 millones de dólares, además de joyas.

Para que un plan –o un proyecto– sea exitoso, sus integrantes deben ser grandes ideólogos, deben estar comprometidos; en una palabra, deben ser unos cracks. Y en esta historia lo fueron: en una época de violencia y muerte, lograron llevarse una fortuna sin disparar un arma ni lastimar a nadie.

Pero su desafío no fue robar, sino a quién y cómo. Ahí es donde se traza el límite de la tolerancia.

Como en todo gran plan, siempre hay un enigma por resolver. La película explica poco y muestra mucho: deja que las imágenes hablen por sí mismas. Y, sin duda, ese es un acierto.

En los primeros minutos, sin diálogo, uno de los protagonistas camina bajo la lluvia. Persigue un cigarrillo hasta que se le escurre en una alcantarilla, justo frente al Banco Río. Esa sola imagen basta para contarnos el nacimiento de una idea, de una obsesión, de un conflicto.

Ahora vamos con El robo del siglo: versión Data Science. Nuestro desafío es revelar ¿quién es quién? en el robo de datos a través de sitios fraudulentos. 😏💻💰

## Contexto

### Objetivo 

Entrenar un modelo de Machine Learning para detectar sitios web de phishing en Argentina basándose en sus características. 

Se utilizará una combinación de datos reales y datos sintéticos para mejorar la calidad del entrenamiento.

**[⬆ Volver al inicio](#introduccion)**

## Contexto_Analítico 

Para entrenar un modelo de Machine Learning, cuantas más observaciones disponibles, mejor será la generalización del modelo. Para generar un mix entre datos reales y datos sintéticos, se plantea de la siguiente manera:

Datos reales

Se extraen la mayor cantidad posible de sitios .ar usando búsquedas automatizadas en Google, scraping de directorios web y bases de datos de dominios. Se obtienen las características princiaples a través de librerías como whois, requests, tldextract, etc. Se procede a estandarizar los registros resultantes y eliminar inconsistencias.

Datos sintéticos

Usando la librería Faker, se generan dominios falsos .ar con características realistas. Se crea una distribución similar a la de los datos reales (por ejemplo, si el 40% de los sitios reales tienen certificados SSL, se refleja esto en los datos sintéticos). Se aplican técnicas como oversampling para balancear las clases.

Al convinar ambos enfoques, obtenemos las siguientes ventajas: ✅ Miles de registros reales (dependiendo de la cantidad de sitios .ar disponibles). ✅ Millones de registros sintéticos sin problema.

Para comenzar, vamos a trabajar con alrededor de 100.000 registros (80% sintéticos, 20% reales) y luego escalar según los avances del proyecto.


Tipo de Archivo | Tamaño | Etiquetas | Estructura de Datos | N° Registros | N° Campos | Link |
|---|---|---|---|---|---|---|
| .CSV | 4,52 Mb| `Establecimientos, Geopandas`   | Tabular | 40.682  | 17 | [Link](https://github.com/NoeliaFerrero/Proyecto_MentoriaFAMAF_2024/blob/932398f852ae3619dedc304d591dc37b4fd871fd/DataSets/Establecimientos-asistenciales-asentados-registro-federal-refes-20220404.csv)|
| .CSV | 20   Kb| `Especialidades Médicas`        | Tabular | 76      | 25 | [Link](https://github.com/NoeliaFerrero/Proyecto_MentoriaFAMAF_2024/blob/main/DataSets/Cant_medicos%20especialistas%20por%20Provincia.csv)|

### Diccionario_de_Datos

|Nombre Archivo | Link |
|---|---|
| Descrip_Data | [Link](https://github.com/NoeliaFerrero/Proyecto_MentoriaFAMAF_2024/blob/1934d95136ef5f2b25d6d71cb2c856353699ece8/DataSets/Descrip_data.csv)|


### Vista_previa_de_los_Datos 

|Notebook | Descripción | Link |
|---|---|---|
| 🐍 Proyecto Sin bajar la Guard.IA | Demo de conexión a los Set de datos | [Link](------https://colab.research.google.com/drive/11ix1h6kQFJaYX3G78KJz68CCpWfgffML?usp=sharing) |
 
**[⬆ Volver al inicio](#introduccion)**

## FAQs

Si te interesó la temática del proyecto, me gustaría compartirte algunas 'Advertencias y Precauciones' relacionadas con la modalidad de trabajo de esta Guard.IA, así podrás tenerlas en cuenta antes de sumergirte en el proyecto...

### Faq1 


***Posología y forma de administración de los resultados hallados durante la mentoria***

🎯  El contexto es clave: proporcionar contexto es el equivalente a brindar un mapa de un hospital. Ayuda tanto a los involucrados en el proyecto, como a cualquier persona externa que tenga alcance al mismo, a “scrollear” a través de los datos, comprendiendo no solo el qué, sino el porqué. 

🩺  Claridad ante todo: al igual que una señal clara de emergencia, nuestros hallazgos deben destacar la información más crítica de manera comprensible a primera vista. La simplicidad muchas veces, no resta valor, lo amplifica. Se trabajará con la Metodología del Diamante como una forma de empezar a detectar/ampliar las ideas iniciales. 

### Faq2 

***Este proyecto esta CONTRAINDICADO para vos en caso de que...***

🚨  NO estes dispuesto/a a iterar end-to-end tantas veces como sea necesario y NO disfrutes afrontar los desafíos que implican los algoritmos de Machine Learning: al igual que los registros médicos interactivos, trabajaremos con las distintas funcionalidades de las librerías para Ciencia de Datos, que nos permitan desarrollar modelos capaces de interpretar y aprender de la naturaleza de los datos seleccionados. Además, apuntando a un enfoque multidimensional y poniendo el foco en las preguntas de interés, cruzaremos los datos bajo estudio con los datos obtenidos en el Censo Nacional 2022 y con información compatible de la API de Google para georreferenciar los establecimientos de salud. Y a medida que vallamos avanzado en el proyecto, se trasladaran los insights obtenidos al framework de Streamlit para convertir los scripts en una data apps y poder mostrarlos de manera más interactiva. Todo en Python puro y open source, no se requiere experiencia en front-end. Trabajando con Generative IA + Steamlit, lograremos el match perfecto.

💊  NO te guste crear visualizaciones con propósito y presentaciones atractivas: los colores y el diseño de la cartelería empleada en un establecimiento hospitalario, claramente no son solo estéticos. Son señales visuales que guían la atención, resaltan diferencias críticas y evocan experiencias. De igual manera, se abordará el proyecto mediante técnicas de storytelling (narrativa visual), por ejemplo, usando atributos preatentivos, esto es, atributos visuales que nuestro cerebro procesa sin necesidad de una acción consciente y trabajaremos con mapas, mapas y mas mapas.

🚑  NO te comprometas a trabajar en equipo: El compromiso es un aspecto que a menudo se pasa por alto en los esfuerzos de colaboración y es fundamental para conseguir resultados de calidad entre las personas que trabajan en un tema concreto. Será necesario dedicar el tiempo suficiente para generar buenos aportes al proyecto, así como para apoyar las iniciativas de todos los integrantes de la mentoría.


**[⬆ Volver al inicio](#introduccion)**

Gracias por haberte detenido en estas coordenadas, espero que te lleves algo útil del tiempo invertido ;) 

By Noe Ferrero
