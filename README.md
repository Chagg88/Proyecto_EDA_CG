# Proyecto EDA - Análisis Campañas Marketing Banco

Descripción del proyecto
Este proyecto realiza un análisis exploratorio de datos (EDA) sobre campañas de marketing telefónico llevadas a cabo por una entidad bancaria portuguesa.
El objetivo es entender mejor el compartamiento de los clientes y detectar patrones que influyen en la suscripción
Se han utilizado herramientas de análisis de datos en Python, enfocándonos en la limpieza, transformación, visualización e interpretación de datos.

Estructura del Proyecto
Proyecto_EDA_CG/
|---Data
|   |---Raw_Data                  # Datos Originales
|        |---bank-additional.csv
|        |---customer-details
|   |---Transformed_Data          # Datos Transformados
|        |---01_Datos_Fusionados_Bank     #Análisis preliminar de los datos y fusión de los datos originales en un dataframe único
|        |---02_Datos_Limpios_Bank        #Limpieza de datos fusionados
|        |---03_Datos_Cat_Limpios_Bank    #Análisis y gestión de nulos de columnas categóricas
|        |---04_Datos_Cat_Num_Limpios_Bank   #Análisis y gestión de nulos de columnas numéricas (output final)
|---Notebooks
|   |---01_EDA_preliminar_bank
|   |---02_Limpieza_datos_bank
|   |---03_Analisis_col_categoricas_bank
|   |---04_Analisis_col_numericas_bank
|---README.md

Instalación y Requisitos
Este proyecto utiliza Python 3.12.2 y requiere las siguientes bibliotecas:
-pandas
-numpy
-matplotlib
-seaborn

Resultados y Conclusiones
Se ha fusionado los ficheros originales de "bank-additional" y de "customer-details" y ha quedado un fichero de 43.170 filas y de 28 columnas.
No existen datos duplicados, cada cliente cuenta con ID único.
Dentro de los datos nulos destacan 3 columnas: Euribor3m (21,83% de nulos), default (21,20% de nulos) y age (12,25% de nulos). El resto de columnas cuenta con un porcentaje de nulos inferior al 5%. Sería conveniente enteder con el cliente como se han generado estos nulos.
Posteriormente se ha realizado un análisis de las columnas categóricas: 'job', 'marital', 'education', 'contact', 'poutcome', 'y':
En la columna job se han identificado 11 valores únicos, casi el 50% de los datos se concentran en admin (25,5% del total) y blue-collar (22,6% del total)
En la columna marital se han identificado 3 valores únicos, el 60,6% corresponde a married, el 28,2% a single y el 11,2% a divorced
En la columna education se han identificado 7 valores únicos, casi el 55% de los datos se concentran en university degree (30,9% del total) y high-school (24,1% del total). Sería conveniente clarificar con el cliente a que se refieren las categorias de basic (9y, 6y, 4y) para ver si podemos agruparla en una solo categoria.
En la columna contact se han identificado 2 valores únicos, el 63,7% corresponde a cellular y el 36,3% a telephone.
En la columna poutcome (resultado de la campaña anterior) se han identificado 3 valores únicos, destaca que en el 86,3% de los clientes no existía campaña previa, en el 10,4% fue una campaña fallida y que únicamente en el 3,3% de los clientes hubo una campaña exitosa.
En la columna y, donde se analiza si los clientes han suscrito o no un producto, destaca que el 88,7% de los clientes no han suscrito productos/servicios.
En lo que respecta a las columnas numéricas, se han identificado outliers en las columnas de age, default, duration, campaign, previous y euribor. Sería interesante comentar con el cliente los outliers para ver si se trata de valores erróneos o si se trata de datos reales que hay que analizar de manera diferente
Se ha decidido sustituir todos los valores nulos por "unkwown".
Este análisis exploratorio ha permitido entender la estructura, calidad y composición de los datos, sentando una base sólida para las etapas posteriores del análisis. La colaboración con el cliente será clave para resolver ciertas ambiguedades y tomar decisiones adecuadas para la preparación de datos.



Próximos Pasos
Realizar un tratamiento avanzado de los valores únicos, consultando y aclarando como se han generado.
Revisión y estandarización de variables categ{oricas (education)
Verificar con expertos del negocio los outlieres detectados y aplicar técnicas estadísticas si fuera necesario.
Realizar un análisis segmentado para explorar los perfiles de los clientes, esto permitiría identificar patrones más finos e identificar como mejorar las campañas de marketing para que los clientes puedan adquirir con mayor frecuencia nuevos productos y/o servicios.
Convertir todos estos insights en sugerencias de valor para poder optimizar las campañas de marketing futuras.
Creación de nuevas columnas identificando los key drivers del marketing aplicado a una entidad bancaria.

Contribuciones
Las contribuciones son bienvenidas.

Autores
Github: @Chagg88
email: cgarcini_m88@hotmail.com
