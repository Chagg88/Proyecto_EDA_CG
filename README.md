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
Se ha fusionado los ficheros originales de "bank-additional" y de "customer-details" y ha quedado un fichero de 43.170 filas y de 28 columnas


Próximos Pasos


Contribuciones
Las contribuciones son bienvenidas.

Autores
Github: @Chagg88
email: cgarcini_m88@hotmail.com
