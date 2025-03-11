# Mentoria FAMAF 2025 

# Proyecto: ***El robo del siglo ~ Un plan secreto para descifrar el detrás de escena de sitios fraudulentos***

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
  - [Este proyecto NO es el indicado para vos en caso de que...](#faq2)

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

Al igual que en El robo del siglo, cada integrante del equipo cumple un rol esencial en el éxito del plan. Participar en este proyecto te permitirá desarrollar habilidades clave en Data Science mientras encarnas a uno de estos perfiles:

🛠️ El Ingeniero (hábil, resolutivo, técnico)

Aprenderemos a diseñar y optimizar pipelines de datos, creando el "túnel" que nos permitirá acceder a la información clave.

🕶️ El Hombre del Traje Gris (analítico, estratégico, discreto)

Dominaremos el análisis exploratorio y la modelización de datos para detectar patrones ocultos, como quien observa sin ser visto.

🗣️ El Negociador (comunicador, persuasivo, adaptable)

Desarrollaremos habilidades para contar historias con datos y presentar hallazgos como un verdadero "negociador" e "interprete" de datos.

👻 El Fantasma (silencioso, preciso, impredecible)

Aprenderemos técnicas avanzadas de scraping y análisis de fraudes para predecir movimientos que a simple vista, se realizan sin dejar rastro en el mundo de los datos.

💰 El Cerebro del Plan (visionario, líder, estratega)

Podremos proponer nuevas estrategias y entre todos los integrandes del proyecto, asegurarnos de que el plan se ejecute a la perfección. 

### Faq2 

***Este proyecto NO es el indicado para vos en caso de que...***

❌ No quieras formar parte de un equipo comprometido.

Aquí no hay lugar para improvisaciones. Como en el robo, cada pieza del plan debe encajar perfectamente.

❌ Prefieras que te den todo servido en vez de investigar y resolver problemas.

Si esperás que el túnel ya esté cavado y la ruta de escape lista, este no es tu golpe. Acá hay que ensuciarse las manos (metafóricamente hablando😏).

❌ No te interese aprender nuevas habilidades.

Si solo querés "estar", pero no "hacer", te va a costar mantenerte en el equipo. Todos aquí tienen un rol y una misión.

❌ Te frustre demasiado encontrar obstáculos o fallar en el primer intento.

Como en cualquier buen robo (o en Data Science), los planes deben ajustarse sobre la marcha. Si te rendís ante el primer muro, este no es tu proyecto.

❌ No te guste analizar datos ni buscar patrones ocultos.

Este proyecto es para quienes disfrutan descifrar enigmas, leer entre líneas y conectar puntos invisibles. Si no te atrae la investigación, la mejor sugerencia que puedo darte, es buscar otro desafío.

**[⬆ Volver al inicio](#introduccion)**

Espero que el tiempo invertido te haya dejado algunos spoilers útiles. Esto es solo el comienzo… nos vemos dentro. 🚀💻

By Noe Ferrero
