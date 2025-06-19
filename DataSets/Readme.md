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



