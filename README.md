# Detección de exoplanetas con redes neuronales usando la base de datos de la misión Kepler

<div align=center>
  <a href="https://www.universidadviu.es/"><img src="https://campus.viu.es/branding/themes/viu_2019/images/logo_viu.svg" alt="Valencian International University" title="Valencian International University" hspace="30" height="128px" /></a>
</div>

Autor: [_Martín Solís, Héctor_][author_profile]

Tutor: [_Guzmán Álvarez, César A._][supervisor_profile]

## Índice

- [Detección de exoplanetas con redes neuronales usando la base de datos de la misión Kepler](#detección-de-exoplanetas-con-redes-neuronales-usando-la-base-de-datos-de-la-misión-kepler)
  - [Índice](#índice)
  - [Resumen](#resumen)
  - [Código](#código)
    - [Ficheros](#ficheros)

## Resumen

La misión Kepler nace para la observación de la galaxia y la detección de planetas con características similares a la tierra, que orbiten alrededor de una estrella similar al Sol. Para poder clasificar estos planetas observados eficientemente, se requiere un procesamiento automatizado y preciso debido a la gran cantidad de observaciones que ha proporcionado esta misión durante años.

En este proyecto se presenta un método de clasificación de estas observaciones utilizando las curvas de luz que emiten estos exoplanetas. Se aplica una clasificación por medio de semejanza con planetas que ya han sido previamente confirmados.

Se utiliza un modelo con Redes Neuronales Convolucionales que permitirán predecir si un planeta es similar a la tierra o no.

## Código

Todo el código usado en este proyecto está dentro del directorio [`proyecto/`](proyecto).
Está totalmente escrito en Python utilizando Jupyter Notebooks.

Alguna de las carpetas que se utilizan en el proyecto que contienen ficheros de gran tamaño no están incluidas en el repositorio debido a limitaciones de espacio. Dichas carpetas son las siguientes:

* [`proyecto/mastDownload`](proyecto/mastDownload): incluye los ficheros FITS descargados del [Portal MAST][mast_portal]. Carpeta auto-generada en el fichero [`proyecto/01.-extraccion_datos_mast.ipynb`](proyecto/01.-extraccion_datos_mast.ipynb)

* [`proyecto/lightkurve`](proyecto/lightkurve): incluye ficheros FITS descargados usando la [librería lightkurve][lightkurve]. Carpeta auto-generada en el fichero [`proyecto/03.-lightkurve_prueba.ipynb`](proyecto/03.-lightkurve_prueba.ipynb)

* [`proyecto/trainings`](proyecto/trainings): include model backups for every epoch of the training step for the neural networks. Carpeta auto-generada en el fichero [`proyecto\06.-rrnn_local.ipynb`](proyecto\06.-rrnn_local.ipynb), [`proyecto\07.-rrnn_global.ipynb`](proyecto\07.-rrnn_global.ipynb) and [`proyecto\08.-rrnn_completa.ipynb`](proyecto\08.-rrnn_completa.ipynb)


### Ficheros


* [01.-extraccion_datos_mast.ipynb](proyecto\01.-extraccion_datos_mast.ipynb): primera aproximacion para la extracción de datos en crudo usando el [Portal MAST][mast_portal] para obtener los ficheros FITS de cada KOI y, tras esto, extraer los datos de curvas de luz a partir de ellos.

* [02.-prueba_csv_con_lightkurve.ipynb](proyecto\02.-prueba_csv_con_lightkurve.ipynb): prueba para combinar las curvas de luz obtenidas en el fichero anterior y procesarlas posteriormente usando la [librería lightkurve][lightkurve]
  
* [03.-lightkurve_prueba.ipynb](proyecto\03.-lightkurve_prueba.ipynb): prueba para usar únicamente la [librería lightkurve][lightkurve] para descargar, tratar y visualizar datos de un único KOI
 
* [04.-extraccion_datos_lightkurve.ipynb](proyecto\04.-extraccion_datos_lightkurve.ipynb): tras no conseguir tratar los datos descargados del MAST para combinarlos con lightkurve, en este fichero se realiza el proceso de descarga de todos los ficheros para cada KOI unicamente con la [librería lightkurve][lightkurve]

* [05.-unification.ipynb](proyecto\05.-unification.ipynb): en este fichero se procesan todos los ficheros obtenidos con la [librería lightkurve][lightkurve], se limpian y procesan para dejarlos listos para usarlos como entrada de las redes neuronales.

* [06.-rrnn_local.ipynb](proyecto\06.-rrnn_local.ipynb): creacion, entrenamiento y analisis de métricas para la red neuronal local.

* [07.-rrnn_global.ipynb](proyecto\07.-rrnn_global.ipynb): creacion, entrenamiento y analisis de métricas para la red neuronal global.

* [08.-rrnn_completa.ipynb](proyecto\08.-rrnn_completa.ipynb): creacion, entrenamiento y analisis de métricas para la red neuronal completa (local + global).

* [09.-metricss.ipynb](proyecto\09.-metricss.ipynb): extracción de metricas para todas las combinaciones probadas para la red neuronal completa

* [10.-ModelAveraging.ipynb](proyecto\10.-ModelAveraging.ipynb): prueba de model averaging y extraccion de metricas usando la mejor configuracion obtenida previamente para la red neuronal completa






[supervisor_profile]: https://scholar.google.com/citations?user=pwRGe0wAAAAJ&hl=es
[author_profile]: https://www.linkedin.com/in/hecmartinsol/
[lightkurve]: https://docs.lightkurve.org
[mast_portal]: https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html