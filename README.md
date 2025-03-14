# Mentoria FAMAF 2025 

<h1 align="center">Proyecto: 🎬 <em>El ROBO del SIGLO DIGITAL</em></h1>  
<h3 align="center">Un plan secreto contra el fraude online</h3>


<div align="center">

<p align="center">
  <img src="https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/bcc026f560f5e02d119e2826ca38789d5b0253b0/portadaV1__cleanup_cleanup.png" width="35%">
</p>
</div>

# Ficha Técnica 📽️
- [Introduccion](#introduccion)
- [Contexto](#Contexto)
  - [Objetivo del Proyecto](#objetivo_del_proyecto)   
- [Contexto Analítico](#Contexto_Analítico)
  - [Diccionario de Datos](#diccionario_de_datos)
  - [Vista previa de los datos](#vista_previa_de_los_datos)
- [FAQs](#faqs)
  - [¿Qué te sumaría participar en este proyecto?](#faq1)
  - [Este proyecto NO es el indicado para vos en caso de que...](#faq2)
  - [¿Cuál es el objetivo final de la mentoria?](#faq3)

## Introduccion 

En 2006, un grupo de ladrones vació el Banco Río de Acassuso, Buenos Aires, sin disparar un solo tiro.

El saqueo quedó instalado en el imaginario social como El robo del siglo. Así lo bautizaron los medios cuando comenzaron a revelarse los detalles de un atraco tan meticuloso que parecía sacado de la mente de un guionista sofisticado: una toma de rehenes con armas de juguete, un túnel de 15 metros para trasladar el dinero, gomones, diques improvisados, la huida a través de las alcantarillas y un botín de 20 millones de dólares, además de joyas.

Para que un plan –o un proyecto– sea exitoso, sus integrantes deben ser grandes ideólogos, deben estar comprometidos; en una palabra, deben ser unos cracks. Y en esta historia lo fueron: en una época de violencia y muerte, lograron llevarse una fortuna sin disparar un arma ni lastimar a nadie.

Pero su desafío no fue robar, sino a quién y cómo. Ahí es donde se traza el límite de la tolerancia.

Como en todo gran plan, siempre hay un enigma por resolver. La película explica poco y muestra mucho: deja que las imágenes hablen por sí mismas. Y, sin duda, ese es un acierto.

En los primeros minutos, sin diálogo, uno de los protagonistas camina bajo la lluvia. Persigue un cigarrillo hasta que se le escurre en una alcantarilla, justo frente al Banco Río. Esa sola imagen basta para contarnos el nacimiento de una idea, de una obsesión, de un conflicto.

Ahora vamos con El robo del siglo: versión Data Science. Nuestro desafío es revelar ¿quién es quién? en el robo de datos a través de sitios fraudulentos. 😏💻💰

## Contexto

### Objetivo_del_Proyecto

El objetivo combina web scraping, análisis exploratorio y machine learning para estudiar el ecosistema web argentino y luego detectar sitios fraudulentos.

Fase 1: 
- Analizar las preferencias digitales de los usuarios en Argentina mediante el scraping del directorio Argendir, clasificando los sitios por categoría y tráfico estimado.
- Ampliar el análisis para detectar sitios web de phishing y fraudes online, con especial atención a la banca electrónica y el comercio digital.
  
Fase 2:
- Entrenar modelos de Machine Learning para detectar sitios web de phishing en Argentina basándose en sus características. Este enfoque inicial está abierto a ampliarse hacia la detección de correos electrónicos maliciosos (spam) y otros tipos de fraudes online, según lo requiera el proyecto. A medida que avancemos, se pondrá especial atención a los sitios de banca electrónica, con el objetivo de fortalecer la protección de los usuarios en estos entornos.

Aclaración:

En la era de la IA, las herramientas de automatización y generación de contenido han reducido drásticamente las barreras para crear sitios web en cuestión de segundos. Esto significa que los modelos de detección de amenazas deben ser cada vez más sofisticados para mantenerse a la par de los atacantes. Para lograrlo, utilizaremos una combinación de datos reales y sintéticos, ya que los fraudes digitales no solo se basan en patrones históricos, sino que también evolucionan constantemente con nuevas estrategias. Estos datos sintéticos nos permitirán simular escenarios de fraude emergentes y entrenar modelos más robustos para identificar amenazas, a medida que se amplía su alcance. 


**[⬆ Volver al inicio](#introduccion)**

## Contexto_Analítico 

Para entrenar un modelo de Machine Learning, cuantas más observaciones disponibles, mejor será la generalización del modelo. Para generar un mix entre datos reales y datos sintéticos, se plantea de la siguiente manera:

Datos reales

Se extraen la mayor cantidad posible de sitios .ar usando búsquedas automatizadas en Google, scraping de directorios web y bases de datos de dominios. Se obtienen las características principales a través de librerías como Whois, Requests, Tldextract, etc. Se procede a estandarizar los registros resultantes y eliminar inconsistencias.

Datos sintéticos

Usando la librería Faker, se generan dominios falsos .ar con características realistas. Se crea una distribución similar a la de los datos reales (por ejemplo, si el 40% de los sitios reales tienen certificados SSL, se refleja esto en los datos sintéticos). Se aplican técnicas como oversampling para balancear las clases.

Al combinar ambos enfoques, obtenemos las siguientes ventajas: 

✅ Miles de registros reales (dependiendo de la cantidad de sitios .ar disponibles). 

✅ Millones de registros sintéticos sin problema.

Los datasets presentados representan una pequeña muestra inicial, extraída como caso de prueba para una categoría específica (por ejemplo, sitios de determinada temática). En el primer entregable se ampliará la cantidad de datos analizados, lo que permitirá generar una comprensión más profunda. Esta estrategia de trabajo, basada en un enfoque iterativo, asegura que el análisis se realice de manera escalonada y controlada, garantizando que los resultados sean consistentes y aplicables a medida que el roadmap avanza...

Es importante resaltar que en la vida profesional real, este proceso de trabajar con una muestra inicial no es algo exclusivo de este caso de uso. En la mayoría de los proyectos de Data Science, primero recibimos una muestra representativa o de prueba para evaluar la calidad y la aplicabilidad de los datos. Solo una vez que damos el visto bueno o quedamos contratados, es cuando obtenemos acceso completo al conjunto de datos. Esta fase inicial es clave para asegurar que los datos cumplen con los requisitos y objetivos del proyecto, permitiendo realizar ajustes antes de trabajar con el volumen de información completo.



Tipo de Archivo | Tamaño | Etiquetas | Estructura de Datos | N° Registros | N° Campos | Link |
|---|---|---|---|---|---|---|
| .CSV | 225  KB| `Sitios Web, Geolocalizacion`   | Tabular | 25      | 13 | [Link](https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/78d42ea5e2df5d23a654e5f2db557109964999da/DataSets/dataset_sitios_reales.csv)|
| .CSV | 2    KB| `Datos Sinteticos`              | Tabular | 50.000  | 10 | [Link](https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/78d42ea5e2df5d23a654e5f2db557109964999da/DataSets/dataset_sintetico.csv)|
| .CSV | 3    KB| `Caso de uso Educacion`         | Tabular | 10      | 4  | [Link](https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/6da755e6abeb592430c55a3f1836a5be6c421d06/DataSets/sitios_argentinos.csv)|

### Diccionario_de_Datos

|Nombre Archivo | Link |
|---|---|
| Descrip_Data | [Link](https://github.com/NoeliaFerrero/Proyecto_Mentoria_FAMAF_2025/blob/c623891c6379b6305300e35ee64df4de292b2c66/DataSets/Diccionario%20de%20Datos)|


### Vista_previa_de_los_Datos 

|Notebook | Descripción | Link |
|---|---|---|
| 🐍 El robo del siglo digital | Demo de conexión a los Set de datos | [Link](https://colab.research.google.com/drive/1rRdB_il4sG2VJXrSnEHvvGv5F8e4JmLt?usp=sharing) |
 
**[⬆ Volver al inicio](#introduccion)**

## FAQs

Como en cualquier gran golpe, el éxito depende de que cada integrante entienda los riesgos y esté listo para la acción. Si esta misión despertó tu interés, quiero compartirte algunas 'reglas del juego' sobre la modalidad de trabajo, para que las tengas en cuenta antes de cruzar la puerta del banco... perdón, quise decir, antes de sumergirte en el proyecto.

### Faq1 

Al igual que en El robo del siglo, cada integrante del equipo cumple un rol esencial en el éxito del plan. Participar en este proyecto te permitirá desarrollar habilidades clave en Data Science mientras encarnas uno de estos perfiles:

🛠️ El Ingeniero (hábil, resolutivo, técnico)
Diseñaremos y optimizaremos pipelines de datos, creando el "túnel" que nos dará acceso a la información clave. 

🕶️ El Hombre del Traje Gris (analítico, estratégico, discreto)
Dominaremos el análisis exploratorio y la modelización de datos para detectar patrones ocultos, como quien observa sin ser visto.

🗣️ El Negociador (comunicador, persuasivo, adaptable)
Aprenderemos a contar historias con datos y presentar hallazgos como verdaderos negociadores e intérpretes de la información.

👻 El Fantasma (silencioso, preciso, impredecible)
Exploraremos técnicas avanzadas de scraping y detección de fraudes para identificar movimientos que, a simple vista, parecen no dejar rastro.

💰 El Cerebro del Plan (visionario, líder, estratega)
Propondremos nuevas estrategias y, junto con el equipo, nos aseguraremos de que el plan se ejecute a la perfección.

### Faq2 

***Este proyecto NO es el indicado para vos en caso de que...***

❌ No estas dispuesto a formar parte de un equipo comprometido.
Aquí no hay lugar para improvisaciones. Como en el robo, cada pieza del plan debe encajar perfectamente.

❌ Preferís que te den todo servido en vez de investigar y resolver problemas.
Si esperás que el túnel ya esté cavado y la ruta de escape lista, este no es tu golpe. Acá hay que ensuciarse las manos (metafóricamente hablando 😏).

❌ No te interesa aprender nuevas habilidades.
Si solo querés "estar", pero no "hacer", te va a costar mantenerte en el equipo. Todos aquí tenemos un rol y una misión.

❌ Te frustra demasiado encontrar obstáculos o fallar en el primer intento.
Como en cualquier buen robo (o en Data Science), los planes deben ajustarse sobre la marcha. Si te rendís ante el primer muro, este no es tu proyecto.

❌ No te gusta analizar datos ni buscar patrones ocultos.
Este proyecto es para quienes disfrutan descifrar enigmas, leer entre líneas y conectar puntos invisibles. Si la investigación no te atrae, lo mejor que podés hacer es buscar otro desafío.

### Faq3

***¿Cuál es el objetivo final de la mentoría?***

Más allá de lo estrictamente académico, en esta mentoría armaremos un proyecto end-to-end de Ciencia de Datos, abordando datos reales y problemáticas de seguridad, el objetivo e impacto final de la mentoría en sí, es compartirles las prácticas laborales/profesionales más comunes en la industria y, desde mi experiencia, ayudarles a estar mejor preparados para aprovechar esa primera oportunidad laboral tan buscada.

**[⬆ Volver al inicio](#introduccion)**

Espero que el tiempo invertido te haya dejado algunos spoilers útiles. Esto es solo el comienzo…nos vemos dentro. 🚀💻

By Noe Ferrero
