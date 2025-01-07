# **Metadata TV: Tablero de Visualización en Tableau**

Este proyecto utiliza un dataset de metadatos de contenidos (películas, series, documentales, entre otros) para construir un tablero de visualización en Tableau. La información está enriquecida con datos adicionales como códigos de países, permitiendo un análisis detallado y visual de la oferta de contenidos de una plataforma.

## **Dataset**
El dataset principal utilizado en este proyecto contiene información sobre:
- **Identificadores**: `asset_id`, `content_id`.
- **Detalles del contenido**: título, tipo (película, serie, documental), año de lanzamiento, categoría, palabras clave, duración, descripción, audiencia objetivo.
- **Información temporal**: fechas de incorporación y vigencia (`start_vod_date`, `end_vod_date`).
- **Ubicación geográfica**: países en los que el contenido está disponible.

El dataset fue obtenido y preprocesado para optimizar su uso en Tableau.

## **Acondicionamiento en Google Colab**
El procesamiento de los datos se realizó en Google Colab y consistió en los siguientes pasos:
1. **Limpieza de Datos**: 
   - Eliminación de valores nulos y registros duplicados.
   - Conversión de formatos de fechas para facilitar su análisis temporal.
2. **Enriquecimiento del Dataset**:
   - Agregación de un archivo complementario con códigos de países para visualizar la disponibilidad de los contenidos en el mapa.
3. **Exportación**:
   - El dataset procesado fue exportado en formato `.xlsx`, listo para ser integrado en Tableau.

Puedes encontrar el notebook utilizado para este acondicionamiento en el archivo [`condicionar_metadata.ipynb`](./condicionar_metadata.ipynb).

## **Archivos Complementarios**
- **`metadata.xlsx`**: El dataset principal que contiene la información sobre los contenidos.
- **`codigos_paises_completo.csv`**: Archivo complementario con los códigos ISO de países, necesario para el análisis geográfico en Tableau.
- **`condicionar_metadata.ipynb`**: Notebook de Google Colab donde se realizó el acondicionamiento del dataset.

## **Tablero en Tableau**
El tablero de Tableau incluye:
- Visualización de la cantidad y tipos de contenidos disponibles.
- Análisis temporal de la incorporación de contenidos.
- Distribución geográfica de la disponibilidad de los contenidos.
- Clasificación por audiencia, categorías y otros criterios.

## **Cómo Ejecutar el Proyecto**
1. Descarga los archivos del repositorio.
2. Abre el archivo `metadata.xlsx` en Tableau (ya esta acondicionado para usarse).
3. Importa el archivo de códigos de países (`codigo_paises_completo.csv`) como fuente secundaria.
4. Vincula los archivos mediante una relacion de uno a muchos teniendo en cuenta en el metadata la columna "Pais de origen" y en el archivo codigos_paises_completo la columna "Código ISO"
6. Diseña o adapta las visualizaciones según tus necesidades.

## **Contribuciones**
¡Las contribuciones son bienvenidas! Si encuentras un problema o tienes una sugerencia para mejorar el proyecto, usa los medios disponibles para hacermelo saber.
