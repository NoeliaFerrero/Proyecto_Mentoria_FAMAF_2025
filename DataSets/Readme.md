Este repositorio contiene los datasets y notebooks asociados al proyecto de deteccion de posibles casos de fraude en sitios web del ecosistema argentino.

## 📂 Estructura de Datos

Los datos se encuentran organizados en dos grandes categorías, separadas en BigQuery:

### 🗂️ Dataset: `SitiosReales`

Contiene información proveniente de scraping y análisis de sitios web reales.

| Tabla                       | Descripción                                             |
|----------------------------|----------------------------------------------------------|
| `dataset_sitios_reales`    | Datos recolectados desde fuentes confiables argentinas.  |
| `resultados_sitios_reales` | Resultados del data enrichment sobre sitios reales.      |
| `sitios_argentinos`        | Conjunto de sitios con extensión `.ar` procesados.       |
| `sitios_argentinos_basico` | Lista inicial reducida de sitios argentinos populares.   |

### 🧪 Dataset: `DatosSinteticos`

Contiene datos generados de manera artificial para entrenar modelos o realizar pruebas controladas.

| Tabla                | Descripción                                        |
|---------------------|-----------------------------------------------------|
| `dataset_sintetico` | Dataset generado con librerías de datos sintéticos. |

## 🔗 Acceso a BigQuery

Todos los datos se encuentran disponibles en el proyecto de Google Cloud:  
`el-robo-del-siglo-463411`

## 📌 Justificación técnica

> Usamos GitHub para controlar versiones del código y tener trazabilidad en los archivos base, mientras que BigQuery se utiliza para el almacenamiento estructurado, consultas SQL eficientes y escalabilidad del análisis de datos.

---

# Guía rápida: Cómo acceder al proyecto en Google Cloud Console

## Paso 1: Acceder a la consola de Google Cloud

Abrí tu navegador e ingresá a la dirección:  
[https://console.cloud.google.com/](https://console.cloud.google.com/)

Si no estás logueada, iniciá sesión con tu cuenta de Google.

## Paso 2: Seleccionar el proyecto "El Robo del Siglo"

En la parte superior de la consola, hacé clic en el nombre del proyecto que aparece (puede decir "No organization" u otro nombre).

Se abrirá una ventana con la lista de proyectos.

Buscá y hacé clic sobre:

**✔️ El Robo del Siglo**  
ID del proyecto: `el-robo-del-siglo-463411`

Una vez seleccionado, se activará ese proyecto para todas tus tareas.

## Paso 3: Acceder a BigQuery

Una vez que estás en el proyecto correcto, podés ir a BigQuery desde:  
[https://console.cloud.google.com/bigquery](https://console.cloud.google.com/bigquery)

Ahí vas a ver los datasets **SitiosReales** y **DatosSinteticos**.

## Verificación

Verificá que estás en el proyecto correcto mirando la esquina superior izquierda de la consola, donde debe decir:

**✅ El Robo del Siglo**

Y la URL debe incluir algo como:

...project=el-robo-del-siglo-463411

# 📁 Guía sobre Dataset vs DataFrame

En el proyecto usamos tanto **DataFrames** en Python como **Datasets** en BigQuery. Aunque suenen parecidos, cumplen funciones muy distintas.

 🟦 ¿Qué es un DataFrame?

Un **DataFrame** es una estructura de datos **en memoria**, propia de Python (usando la librería `pandas`), el cual podemos pensar como una **tabla temporal** que se usa dentro del entorno de análisis, como Google Colab.

### Características principales:
- Pertenece a la librería `pandas`
- Está en tu entorno de trabajo (Colab, Jupyter, etc.)
- Permite análisis, filtrado, agrupamiento, visualización
- Se borra cuando se cierra el entorno (a menos que lo guardes)
- Ideal para trabajar en notebooks de forma exploratoria

### Ejemplo:
```python
import pandas as pd
df = pd.read_csv("archivo.csv")
```

## 🟥 ¿Qué es un Dataset?
Un Dataset, en el contexto de BigQuery, es un contenedor lógico de tablas en la nube. Es una unidad de almacenamiento persistente y escalable, muy útil para proyectos en producción o colaborativos.

### Características principales:
-Vive en Google BigQuery (persistente en la nube)
- Contiene múltiples tablas relacionadas
- Se accede y consulta con SQL
- Puede compartirse fácilmente con otras personas
- Escalable y profesional

### Ejemplo en BigQuery:
Dataset: SitiosReales
Tabla: sitios_argentinos_basico

📊 Comparación rápida

|Concepto               | DataFrame (pandas)                                      | Dataset (BigQuery)                                      |
|-----------------------|---------------------------------------------------------|---------------------------------------------------------|
| ¿Dónde vive?          | En memoria (Colab, local)                               |En la nube (Google BigQuery)                             |
| ¿Qué contiene?        | Datos en forma de tabla                                 |Tablas (como archivos grandes en SQL)                    |
| ¿Temporal?            | Sí                                                      |No (persistente)                                         |
| ¿Se comparte?         | Difícil sin guardarlo                                   |	Fácil con permisos y acceso en GCP                      |
| ¿Para qué sirve?      | Análisis, visualización, modelo                         |Almacenamiento profesional y consultas                   |


🧠 ¿Por qué usamos ambos en este proyecto?
BigQuery permite almacenar y consultar grandes volúmenes de datos de forma escalable y segura.
Los notebooks en Colab usan DataFrames para analizar, visualizar y modelar los datos dinámicamente.
La combinación de ambas herramientas nos permite tener un entorno profesional, colaborativo y accesible para todos los integrantes del proyecto.




