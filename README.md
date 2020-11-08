# Detección de exoplanetas con redes neuronales usando la base de datos de la misión Kepler

<div align=center>
  <a href="https://www.universidadviu.es/"><img src="https://campus.viu.es/branding/themes/viu_2019/images/logo_viu.svg" alt="Valencian International University" title="Valencian International University" hspace="30" height="128px" /></a>
</div>

Author: [_Martín Solís, Héctor_][author_profile]

Supervisor: [_Guzmán Álvarez, César A._][supervisor_profile]

## Table of Contents

- [Detección de exoplanetas con redes neuronales usando la base de datos de la misión Kepler](#detección-de-exoplanetas-con-redes-neuronales-usando-la-base-de-datos-de-la-misión-kepler)
  - [Table of Contents](#table-of-contents)
  - [Abstract](#abstract)
  - [Code](#code)

## Abstract

Kepler mission was created to observe the galaxy and detect planets with similar characteristics to the Earth, which orbit around a star similar to the Sun. In order to classify these observed planets efficiently, automated and accurate processing is required due to the large number of observations this mission has provided over the years.

This project presents a method of classifying these observations using the light curves that these exoplanets emit. A classification is applied by means of similarity with planets that have already been confirmed.

A model with Convolutional Neural Networks is used and it will allow to predict if a planet is similar to the earth or not.

## Code

All code used in this project is available inside [`proyecto/`](proyecto) directory.
It is fully written in Python using Jupyter Notebooks.

Some of the folders which large data files or tranings files, are not included in this repository due to memory limitations.

Those folders are included
* [`proyecto/mastDownload`](proyecto/mastDownload): includes FITS files downloaded from MAST portal. Auto-created on [`proyecto/01.-extraccion_datos_mast.ipynb`](este)
* [`proyecto/lightkurve`](lightkurve): include
* [`proyecto/trainings`](trainings)


[supervisor_profile]: https://scholar.google.com/citations?user=pwRGe0wAAAAJ&hl=es
[author_profile]: https://www.linkedin.com/in/hecmartinsol/