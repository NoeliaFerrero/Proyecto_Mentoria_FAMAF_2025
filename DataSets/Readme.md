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
