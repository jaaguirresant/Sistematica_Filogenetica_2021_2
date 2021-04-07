# Sistematica-Filogenetica

# MÓDULO INFERENCIA FILOGENÉTICA


## Objetivos

1. Aprender las bases metodológicas de los principales métodos de inferencia filogenética a partir de matrices de caracteres homólogos y evaluar críticamente los supuestos, virtudes y desventajas de estos métodos.

2. Conocer los principios estadísticos para medición de la confianza de las hipótesis filogenéticas.  

3. Adquirir destrezas computacionales para llevar a cabo análisis de inferencia filogenética a partir de matrices de caracteres empíricas.

## Competencias

1. Habilidad de inferir e interpretar críticamente hipótesis de relaciones filogenéticas en cualquier grupo de organismos generadas bajo distintas metodologías a partir de matrices de caracteres.

2. Capacidad para interpretar fundamentos de la biología evolutiva en un árbol filogenético generado a partir de matrices de caracteres empíricas.

3. Entendimiento de la importancia de la inferencia filogenética para abordar problemas biológicos en un contexto evolutivo.

## Estructura general del módulo

### Preparación

Este módulo ha sido diseñado para estudiantes del curso de posgrado "Sistemática Filogenética y Nomenclatura Botánica/Zoológica" del programa de Maestría en Ciencias-Biología de la Universidad Nacional de Colombia. Los estudiantes inscritos en este curso ya debieron haber tomado cinco semanas de temas introductorios sobre evolución y sistemática filogenética para poder seguir con los contenidos de este módulo. Este módulo fue diseñado para ser tomado de manera remota dada la emergencia generada por el virus COVID-19. 

#### Los requerimientos y materiales básicos para llevar a cabo este módulo son los siguientes:

A. Computador o laptop con los siguientes programas instalados: 
- Editor de texto (recomendados notepad++ para Windows y Atom para Mac).
- [Mesquite](https://www.mesquiteproject.org/). Útil para construir y/o visualizar matrices de caracteres.
- R y R Studio (bajar los paquetes: Ape, Claddis, Phangorn, Phytools).
- [TNT](http://www.lillo.org.ar/phylogeny/tnt/). GUI solo para Windows. Para análisis de Máxima Parsimonia.
- [jmodelTest](https://github.com/ddarriba/jmodeltest2). Para selección de modelos evolutivos de secuencias de nucleótidos.
- [RAxML-GUI](https://antonellilab.github.io/raxmlGUI/). Para análisis de Máxima Verosimilitud.
- [MrBayes](http://nbisweden.github.io/MrBayes/download.html). Para análisis de Inferencia Bayesiana.
- [ASTRAL](https://github.com/smirarab/ASTRAL/blob/master/README.md). Para inferencia de árboles de especies a partir de árboles de genes.
- [FigTree](https://github.com/rambaut/figtree/releases). Para visualización y edición de árboles filogenéticos.
- [Tracer](https://github.com/beast-dev/tracer/releases/tag/v1.7.1). Para visualizar resultados de MCMC.

**Nota:** Es posible que usemos otros programas, pero les avisaré con tiempo. Todos los programas de inferencia filogenética vienen acompañados con sus respectivos tutoriales. Se sugiere seguirlos en su tiempo libre; no se limiten únicamente a los ejercicios de la clase.  

B. Disponibilidad técnica (conexión a internet) para las sesiones virtuales. Si tiene problemas para conectarse, ponerse en contacto directamente conmigo con suficiente anticipación (jaaguirresa@unal.edu.co).

### Dinámica de las clases

Para facilitar el trabajo autónomo de los estudiantes desde sus casas y minimizar la presencialidad en las sesiones virtuales, este módulo está principalmente enfocado en talleres y lecturas en casa. Las sesiones virtuales estarán limitadas a clases cortas sobre conceptos fundamentales de los métodos, explicación de las tareas, resolución de dudas y presentación de resultados. Todas las presentaciones con diapositivas, artículos y talleres serán subidos a esta plataforma en su debido momento. Se recomienda enfáticamente replicar los ejercicios practicados en clase con los datos de sus proyecto de semestre.

## Contenido

**[Clase 1](/clase_1/Taller_matrices.md).**

**PARTE 1. Repaso y corto taller de manejo de matrices y datos en R.** se hará un breve repaso de los recursos informáticos para construcción de matrices con editor de texto, el programa Mesquite y R. Descargar la presentación [aquí](/clase_1/Clase_1.pdf). Para esta parte se deben descargar las siguientes matrices para este ejercicio: [ADN.tnt](/clase_1/ADN.tnt), [morfologia.tnt](/clase_1/morfologia.tnt),[morfologia.nex](/clase_1/morfologia.nex), [ADN.nex](/clase_1/ADN.nex), [ADN.phy](/clase_1/ADN.phy). 

**[Ir al taller aquí](/clase_1/Taller_matrices.md)**

**PARTE 2.Taller de visualización y manipulación de archivos de árboles filogenéticos.** Para esta parte de la clase haremos un ejercicio práctico en R para visualizar y manipular árboles filogenéticos 

**[Ir al taller aquí](/clase_5/Taller_arboles.md)**

#

** Clase 2. Presentaciones de proyectos semestrales**

#

**[Clase 3](/clase_2/clase_2.pdf). Inferencia Filogenética: orígenes, criterio de optimalidad y máxima parsimonia.** Esta clase hace una breve mención a los métodos que dieron origen a los métodos modernos de inferencia filogenética. Además, se define el concepto de "criterio de optimalidad" para la inferencia filogenética y se presenta el primer método que incorpora este criterio: la Máxima Parsimonia (Descargar diapositivas [aquí](/clase_2/clase_2.pdf))

<p align="center">
  <img src="https://github.com/jaaguirresant/Sistematica-Filogenetica/blob/master/Clase_3/Strict.png" width="250" height="200" />
</p>

Como complemento de la clase, cada estudiante deberá hacer el siguiente taller y subirlo al Drive hasta el miércoles 14 de abril de 2021:

**[Ir al taller aquí](/clase_2/Taller_2.md)**


**_NOTA:_** Leer los siguientes artículos para la clase del miércoles 7 de abril de 2021:

- Argumentación Hennigiana y Máxima Parsimonia: [Wiley & Lieberman 2011 - Capítulo 6](/clase_2/MP_Wiley_Lieberman.pdf)

- [González 1999](/Clase_3/Gonzalez_1999_Aristolochia.pdf)

#

**[Clase 4](/clase_4/Taller_MP2.md). Búsqueda de árboles óptimos, medidas de confianza y práctica máxima parsimonia.** En la primera mitad de esta clase se explica el problema de la búsqueda de árboles óptimos en relación al número de taxones, así como las estrategias exactas y heurísicas para explorar el "espacio" de árboles posibles y árboles óptimos. Además, se explican los métodos tradicionales para medir la confianza en las hipótesis filogenéticas ([Descargar diapositivas aquí](/clase_4/clase_4.pdf)). En la segunda mitad de la clase se discutirá el artículo de [González 1999](/clase_3/Gonzalez_1999_Aristolochia.pdf). Como complemento para la discusión del artículo es necesario leer y responder las preguntas del siguiente enlace: 

[Taller artículo González (1999)](/clase_5/Taller_Lectura_Gonzalez_1999.md). Subir las respuestas al Drive a más tardar el miércoles 14 de abril.

Finalmente, esta clase termina con una corta práctica computacional de inferencia filogenética con Máxima Parsimonia usando el programa TNT y el paquete Phangorn de R. **[ir al taller aquí](/clase_4/Taller_MP2.md)**


**_NOTA:_** Para la clase del jueves y viernes leer:

1. Modelos evolutivos: [Strimmer & Haeseler 2009](/clase_4/Modelos.pdf).

2. Filogenética paramétrica: [Wiley & Lieberman 2011 - Capítulo 7](/clase_4/Parametric_Phylogenetics.pdf).

3. Atracción de ramas largas: [Philippe et al. 2005](/clase_4/LBA_2005.pdf).

#

**Clase 5. Modelos evolutivos.** Esta clase se destinan a entender los conceptos básicos del uso de modelos evolutivos explícitos para la inferencia filogenética usando la máxima verosimilitud como criterio de opimalidad ([Descargar diapositivas aquí](/clase_7/clase_7.pdf)). Como parte práctica, se hará un ejercicio demostrativo sobre la escogencia de modelos usando jModelTest y R.

<p align="center">
  <img src="https://github.com/jaaguirresant/Sistematica-Filogenetica/blob/master/clase_7/Imagen_c7.jpg" width="250" height="270" />
</p>

**TAREA:** Leer los siguientes artículos y responder las preguntas del siguiente taller [Cuestionario LBA y modelos evoltivos](/clase_6/Taller_Lectura_Modelos.md)

1. Filogenética paramétrica: [Wiley & Lieberman 2011 - Capítulo 7](/clase_4/Parametric_Phylogenetics.pdf).

2. Atracción de ramas largas: [Philippe et al. 2005](/clase_4/LBA_2005.pdf).

#

**[Clase 6](/clase_7/Taller_ML_1.md). Máxima verosimilitud.** Esta clase se divide en dos partes:

1. Charla sobre los fundamentos de la máxima verosimilitud como criterio de opimalidad ([Descargar diapositivas aquí](/clase_7/clase_7.pdf)). 

   - **Tarea.** Realizar los ejercicios del siguiente taller: [TALLER MV](/clase_7/Taller_ML_1.md)

2. Taller de inferencia filogenética usando la Máxima Verosimilitud en R: [ir al Script de R aquí](/clase_8/ML.R). Para este taller usaremos la matriz de ADN de primates del siguiente enlace: [ADN.nex](/clase_1/ADN.nex). 

   - **NOTA:** Se recomienda que los estudiantes realicen el ejercicio previo a la clase y se preparen para explicarlo. Casi todo el ejercicio fue tomado y modificado del siguiente artículo: [Schliep (2019)](/clase_8/Phangorn.pdf).

   - **Tarea.** Responder las preguntas del Script. 

#

**Clase 7. Inferencia Bayesiana.** El objetivo de esta clase es el de aprender como implementar la estadística bayesiana en el contexto de la inferencia filogenética. Para esto, presentaré una corta clase de conceptos fundamentales (bajar diapositivas [aquí](/clase_9/clase_9.pdf) y haremos un ejercicio práctico de inferencia filogenética con el programa [MrBayes](http://nbisweden.github.io/MrBayes/download.html).

<p align="center">
  <img src="https://anabelforte.com/wp-content/uploads/2020/04/Thomas_Bayes.gif" width="250" height="270" />
</p>

Para la práctica usaremos la matriz [primates.nex](/clase_9/primates.nex) y seguiremos el siguiente tutorial: http://mrbayes.sourceforge.net/mb3.2_manual.pdf

**Nota:** Las siguientes lecturas son excelentes complementos para la clase: [Hueselnbeck & Roquist (2004)](/clase_9/Bayesiano_1.pdf) y [Huelsenbeck et al (2002)](/clase_9/Bayesiano_2.pdf)

**Tarea:** Leer para la próxima clase el siguiente artículo: [Sanderson & Schauffer (2002)](/clase_9/Lectura.pdf).

#

### Semana 3

**Clase 8. Evaluación crítica de hipótesis filogenéticas** En esta clase estudiaremos de forma crítica algunos aspectos metodológicos y biológicos generales que deben tenerse en cuenta en los análisis de inferencia filogenética. Para esto haremos una corta clase donde mencionaremos estos aspectos y algunas ayudas metodológicas para sobrellevarlos ([bajar diaposistivas acá](/clase_10/Clase_10.pdf)). La clase se complementa con un taller sobre los temas aprendidos ([Ir al Taller](/clase_10/Taller_clase_10.md)).

<p align="center">
  <img src="https://www.researchgate.net/publication/330808851/figure/fig1/AS:721682977275905@1549074038961/Effect-of-introgression-and-incomplete-lineage-sorting-ILS-in-molecular.png" width="350" height="250" />
</p>

[Fuente de la imagen](https://www.researchgate.net/publication/330808851/figure/fig1/AS:721682977275905@1549074038961/Effect-of-introgression-and-incomplete-lineage-sorting-ILS-in-molecular.png)

#

**Clase 9. Sistemática Filogenética en la práctica** Para esta clase presentaremos dos estudios empíricos de sistemática filogenética realizados por investigadores colombianos. Esta actividad tiene dos propósitos: (1) que los estudiantes se empapen de la investigación en filogenética que hacen los investigadores colombianos, y (2) analizar de una manera crítica las estrategias metodológicas, preguntas de investigación y conclusiones de este tipo de investigaciones. Como preparación para esta actividad, los estudiantes deberán leer los siguientes artículos:

- [Clark, J. L., Clavijo, L., & Muchhala, N. (2015). Convergence of anti-bee pollination mechanisms in the Neotropical plant genus Drymonia (Gesneriaceae). Evolutionary Ecology, 29(3), 355-377.](/clase_11/Clavijo.pdf)

- [Aguirre-Santoro, J., Michelangeli, F. A., & Stevenson, D. W. (2016). Molecular Phylogenetics of the Ronnbergia Alliance (Bromeliaceae, Bromelioideae) and insights into their morphological evolution. Molecular phylogenetics and evolution, 100, 1-20.](/clase_11/Aguirre.pdf)

Para esta clase es necesario que los estudiantes preparen por lo menos tres preguntas sobre los tres principales componentes del estudio: la pregunta de investigación, los métodos y las conclusiones. En el caso de los métodos, pueden hacer preguntas detalladas sobre los muestreos de taxones y caracteres, método de inferencia escogido, modelos evolutivos, medidas de soporte y supuestos biológicos de los sistemas de estudio. 

#

**Clase 10. Presentación de proyectos finales** 

Tiempo para cada presentación: 30 minutos (incluyendo tiempo para preguntas).
