Participantes:  Ketty Rodríguez Bacilio
                Jorge Martinez Guerrero

# 1.	Introducción 
El presente trabajo tiene como objetivo demostrar el uso práctico de herramientas de análisis y procesamiento de datos utilizando el entorno de desarrollo Jupyter Notebook. A partir de un archivo CSV con información estructurada, se llevan a cabo operaciones de carga, segmentación, visualización y almacenamiento de datos, aplicando librerías como Pandas, SQLite3 y Matplotlib.
Este ejercicio busca fortalecer habilidades en la manipulación eficiente de conjuntos de datos, la integración de fuentes diversas y el uso de bases de datos relacionales para su posterior consulta. Asimismo, se enfatiza la importancia de documentar el flujo de trabajo y estructurar los procesos en pasos lógicos, lo cual facilita la trazabilidad y comprensión del análisis realizado. El enfoque aplicado es útil en contextos académicos, investigativos e industriales donde el manejo de datos resulta esencial.

# 2.	Marco teórico de las tecnologías 
Pandas: es una biblioteca de código abierto de Python para el análisis de datos. Le da a Python la capacidad de trabajar con datos similares a hojas de cálculo para una carga rápida de datos, manipulación, alineación y combinación, entre otras funciones. Para proporcionar estas funciones mejoradas a Python, Pandas introduce dos nuevos tipos de datos: Series y DataFrame. El DataFrame representa toda tu hoja de cálculo o datos en forma de tabla, mientras que la Series es una sola columna del DataFrame. Un DataFrame de Pandas también puede considerarse como un diccionario o colección de objetos [1].
Numpy: proporciona una base sobre la que se construyen otros paquetes de ciencia de datos, incluidos SciPy, Scikit-learn y Pandas. NumPy es el paquete fundamental para la computación científica en Python. Su nombre es un acrónimo de Numeric Python o Numerical Python. El núcleo del paquete NumPy es el objeto ndarray (n dimensional array - matriz n-dimensional), que encapsula matrices n-dimensionales de tipos de datos homogéneos, con muchas operaciones que se realizan en código compilado para un mejor rendimiento. El módulo proporciona una gran biblioteca de funciones matemáticas de alto nivel para operar con estas matrices [2].
Matplotlib es una librería completa para crear visualizaciones estáticas, animadas e interactivas en Python [3]. Proporciona múltiples funcionalidades para crear diagramas, gráficos y otras visualizaciones, siendo muy eficiente en la realización de una amplia gama de tareas, además de exportar los gráficos a los formatos más comunes como PDF, SVG, JPG, PNG, BMP y GIF [4].
Sqlite3 es una biblioteca C que proporciona una base de datos ligera basada en disco que No requiere un proceso de servidor separado y permite acceder a la base de datos utilizando una variante no estándar del lenguaje de consulta SQL. Algunas aplicaciones pueden usar SQLite para el almacenamiento interno de datos [5]. 
Polars es una biblioteca de DataFrame increíblemente rápida para manipular datos estructurados. El núcleo está escrito en Rust, y disponible para Python, R y NodeJS. El objetivo de Polars es proporcionar una biblioteca de DataFrame ultrarrápida que:
	Utiliza todos los núcleos disponibles en su máquina.
	Optimiza las consultas para reducir las asignaciones innecesarias de trabajo o memoria.
	Maneja conjuntos de datos mucho más grandes que la RAM disponible.
	Una API coherente y predecible.
	Se adhiere a un esquema estricto (los tipos de datos deben conocerse antes de ejecutar la consulta).[6]
Pygwalker se llama así como una abreviatura de "Python binding of Graphic Walker". Integra Jupyter Notebook. Permite a los científicos de datos visualizar/limpiar/anotar los datos con simples operaciones de arrastrar y soltar e incluso consultas en lenguaje natural. Puede simplificar el flujo de trabajo de análisis de datos y visualización de datos de Jupyter Notebook, convirtiendo el marco de datos de Panda en una interfaz de usuario interactiva para la exploración visual. [7]
Bokeh es una biblioteca de Python para crear visualizaciones interactivas para navegadores web. Te ayuda a crear hermosos gráficos, que van desde tramas simples hasta paneles complejos con conjuntos de datos de transmisión. Con Bokeh, puedes crear visualizaciones con tecnología de JavaScript sin necesidad de escribir JavaScript usted mismo.[8]

# 3.	Descripción del dataset usado 
El dataset usado en el proyecto corresponde a la información recolectada entre los años 2013 y 2022 con relación a las personas que realizaron el registro del proceso de admisión dentro de la Universidad Estatal Península de Santa Elena, el mismo que contiene información básica de los ciudadanos como nombres, apellidos, genero, carrera, fecha de acceso entre otros. El dataset se usará para identificar la cantidad de ciudadanos que realizaron el proceso de admisión y la demanda de las carreras durante los años descritos anteriormente en base a Python y las librerías estudiadas durante el transcurso del módulo.

# 4.	Descripción de los pasos realizados en el proyecto 
### Pasos para genera la base de datos sql

Paso 1: Importar Librerías
Se importan las librerías necesarias para manejar datos (pandas), bases de datos SQLite (sqlite3) y manipular archivos (os).

Paso 2: Cargar el archivo CSV como DataFrame
Se carga el archivo CSV ubicado en la carpeta 'data' y se convierte en un DataFrame de pandas.

Paso 3: Seleccionar columnas H a O (índices 7 a 14)
Se extraen las columnas H a O (índices 7 al 14) del DataFrame original para trabajar solo con esa parte de los datos.

Paso 4: Guardar columnas H-O en base de datos SQLite
Se establece la ruta y nombre de una base de datos SQLite donde se almacenarán las columnas H-O.

Paso 5: Guardar columnas A a G en un nuevo archivo CSV
Se separan las columnas A a G del DataFrame y se guardan en un nuevo archivo CSV llamado Data2.csv.

### Pasos en el archivo Main

Paso 1: Paso 1 Importación de librerías
Este paso corresponde a: paso 1 importación de librerías.

Paso 2: Paso 2 Cargamos Data2.csv
Este paso corresponde a: paso 2 cargamos data2.csv.

Paso 3: Paso 3 Cargamos data_2.db de la base de datos sql
Este paso corresponde a: paso 3 cargamos data_2.db de la base de datos sql.

Paso 4: Paso 4 Unimos las 2 bases de datos
Este paso corresponde a: paso 4 unimos las 2 bases de datos.

Paso 5: Visualizamos la cantidad de campos nulos
Este paso corresponde a: visualizamos la cantidad de campos nulos.

Paso 6: Tomamos un estudiante de muestra y procedemos a crear datos random
para ir realizando los cambios al dataframe y no perder la mayoría de los datos
Este paso corresponde a: tomamos un estudiante de muestra y procedemos a crear datos random
para ir realizando los cambios al dataframe y no perder la mayoría de los datos.

Paso 7: Cambiamos fechas de nacimiento con valores NUll a valores random
Este paso corresponde a: cambiamos fechas de nacimiento con valores null a valores random.

Paso 8: Remplazamos valores nulos por valores random de provincias
Este paso corresponde a: remplazamos valores nulos por valores random de provincias.

Paso 9: Remplazamos cantones
Este paso corresponde a: remplazamos cantones.

Paso 10: Cambiamos la nacionalidad a ecuatoriana si es nulo el campo o si es diferente a la palabra “Ecuatoriana”
Este paso corresponde a: cambiamos la nacionalidad a ecuatoriana si es nulo el campo o si es diferente a la palabra ecuatoriana.

Paso 11: Cambiamos el género de F y M a Femenino y Masculino respectivamente
Este paso corresponde a: cambiamos el género de f y m a femenino y masculino respectivamente.

Paso 12: Eliminamos las filas vacías de genero
Este paso corresponde a: eliminamos las filas vacías de género.

Paso 13: Cambiamos todas las columnas a mayúsculas
Este paso corresponde a: cambiamos todas las columnas a mayúsculas.

Paso 14: Eliminamos Espacios en blanco Iniciales y finales
Este paso corresponde a: eliminamos espacios en blanco iniciales y finales.

Paso 15: Generamos un dataFrame antes de guardar el archivo final
Este paso corresponde a: paso 5 generamos un dataframe antes de guardar el archivo final.

Paso 16: Generamos la ruta parquet y la leemos
Este paso corresponde a: paso 6 generamos la ruta parquet y la leemos.

Paso 17: Instalamos polar e importamos una variable matplotlib y polars
Este paso corresponde a: paso 7 instalamos polar e importamos una variable matplotlib y polars.

Paso 18: Creación de gráfico matplotlib
Este paso corresponde a: creación de gráfico matplotlib.

Paso 19: Uso de PyGWalker
Este paso corresponde a: paso 8 uso de pygwalker.

Paso 20: Generación de gráfico con Bokeh y realizamos el agrupamiento por carrera
Este paso corresponde a: paso 9 generación de gráfico con bokeh.

# 5.	Conclusiones
El desarrollo de este trabajo nos permitió aplicar de manera estructurada conocimientos fundamentales en ciencia de datos, programación en Python y manejo de bases de datos. A través del entorno Jupyter Lab, se logró importar, limpiar y segmentar datos de un archivo CSV, diferenciando conjuntos relevantes de información mediante la separación por columnas específicas. Posteriormente, estos datos fueron almacenados en distintos formatos: uno en una base de datos SQLite y otro en un nuevo archivo CSV, demostrando habilidades en persistencia de datos.
Además, se integraron y visualizaron datos provenientes de múltiples fuentes, fomentando la reutilización y escalabilidad del flujo de trabajo. Este tipo de procesamiento conocido por sus siglas en inglés EDA (Exploratory Data Analysis), no solo optimiza tareas repetitivas, sino que también establece una base sólida para análisis posteriores, visualización de datos y toma de decisiones informadas en aprendizaje de máquina. El trabajo realizado refuerza la importancia de dominar herramientas como Pandas, SQLite y JupyterLab en contextos académicos y científicos.

# 6.	Bibliografía.
[1] Chen, D. Y. (2017). Pandas for everyone: Python data analysis. Addison-Wesley Professional.
https://books.google.es/books?id=7zhDDwAAQBAJ&lpg=PT18&ots=vJvCD8uQqr&dq=pandas%20python&lr&hl=es&pg=PT18#v=onepage&q=pandas%20python&f=false
[2] Prieto Morlanés, J. L. (2024). Matemáticas y gráficos con Python: (1 ed.). Madrid, RA-MA Editorial. Recuperado de https://0410n0tzp-y-https-elibro-net.dossierp.museknowledge.com/es/ereader/upse/273936?page=245.
[3] Matplotlib: Visualization with Python. https://matplotlib.org/
[4] Prieto Morlanés, J. L. (2024). Matemáticas y gráficos con Python: (1 ed.). Madrid, RA-MA Editorial. Recuperado de https://0410n0tzp-y-https-elibro-net.dossierp.museknowledge.com/es/ereader/upse/273936?page=86.
[5] sqlite3 — DB-API 2.0 interface for SQLite databases. https://docs.python.org/3/library/sqlite3.html
[6] Polars user guide. https://docs.pola.rs/#key-features
[7] PyGWalker. https://docs.kanaries.net/pygwalker/index
[8] Bokeh. https://bokeh.org/

