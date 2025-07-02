# 📊 Proyecto EDA - Análisis Campañas Marketing Banco

## 📝 Descripción del proyecto

Este proyecto realiza un análisis exploratorio de datos (EDA) sobre campañas de marketing telefónico llevadas a cabo por una entidad bancaria portuguesa.

El objetivo es entender mejor el comportamiento de los clientes y detectar patrones que influyen en la suscripción.  
Se han utilizado herramientas de análisis de datos en Python, enfocándonos en la limpieza, transformación, visualización e interpretación de datos.

---

## 🗂️ Estructura del Proyecto

```
Proyecto_EDA_CG/
├── Data/
│   ├── Raw_Data/                        # Datos Originales
│   │   ├── bank-additional.csv
│   │   └── customer-details
│   └── Transformed_Data/               # Datos Transformados
│       ├── 01_Datos_Fusionados_Bank
│       ├── 02_Datos_Limpios_Bank
│       ├── 03_Datos_Cat_Limpios_Bank
│       └── 04_Datos_Cat_Num_Limpios_Bank
│
├── Notebooks/
│   ├── 01_EDA_preliminar_bank
│   ├── 02_Limpieza_datos_bank
│   ├── 03_Analisis_col_categoricas_bank
│   └── 04_Analisis_col_numericas_bank   # Output final
│
└── README.md
``` 

---

## ⚙️ Instalación y Requisitos

Este proyecto utiliza **Python 3.12.2** y requiere las siguientes bibliotecas:

- `pandas`  
- `numpy`  
- `matplotlib`  
- `seaborn`

---

## ✅ Resultados y Conclusiones

Se han fusionado los ficheros originales de `"bank-additional"` y de `"customer-details"`, quedando un fichero de **43.170 filas y 28 columnas**.

- **No existen datos duplicados**, cada cliente cuenta con ID único.
- Dentro de los datos nulos destacan 3 columnas:
  - `Euribor3m` (21,83% de nulos)  
  - `default` (21,20%)  
  - `age` (12,25%)  

El resto de columnas cuenta con un porcentaje de nulos inferior al 5%.  
Sería conveniente entender con el cliente cómo se han generado estos nulos.

---

### 🔠 Columnas categóricas

Se realizó un análisis de las columnas categóricas:  
`job`, `marital`, `education`, `contact`, `poutcome`, `y`

- `job`: 11 valores únicos  
  Casi el 50% de los datos se concentran en:
  - `admin` (25,5%)
  - `blue-collar` (22,6%)

- `marital`: 3 valores únicos  
  - 60,6% `married`  
  - 28,2% `single`  
  - 11,2% `divorced`

- `education`: 7 valores únicos  
  - 30,9% `university degree`  
  - 24,1% `high-school`  
  - Requiere clarificación de las categorías `basic (9y, 6y, 4y)` para posible agrupación.

- `contact`: 2 valores únicos  
  - 63,7% `cellular`  
  - 36,3% `telephone`

- `poutcome`: 3 valores únicos  
  - 86,3% no tenían campaña previa  
  - 10,4% campaña fallida  
  - 3,3% campaña exitosa

- `y`: 88,7% de los clientes **no** han suscrito productos/servicios

---

### 📈 Columnas numéricas

Se han identificado **outliers** en las columnas:

- `age`
- `default`
- `duration`
- `campaign`
- `previous`
- `euribor`

Sería interesante comentar con el cliente si se trata de valores erróneos o reales que hay que analizar de manera diferente.

> Se ha decidido sustituir todos los valores nulos por `"unknown"`.

Este análisis exploratorio ha permitido entender la estructura, calidad y composición de los datos, sentando una base sólida para las etapas posteriores del análisis.

> La colaboración con el cliente será clave para resolver ciertas ambigüedades y tomar decisiones adecuadas para la preparación de datos.

---

## 🔜 Próximos Pasos

- Realizar un tratamiento avanzado de los valores únicos, consultando y aclarando cómo se han generado.  
- Revisión y estandarización de variables categóricas (`education`).  
- Verificar con expertos del negocio los outliers detectados y aplicar técnicas estadísticas si fuera necesario.  
- Realizar un análisis segmentado para explorar los perfiles de los clientes.  
- Identificar patrones más finos y mejorar campañas de marketing.  
- Convertir insights en sugerencias de valor para campañas futuras.  
- Crear columnas con los *key drivers* del marketing aplicado a una entidad bancaria.

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas.

---

## 👤 Autor

- GitHub: [@Chagg88](https://github.com/Chagg88)  
- Email: [cgarcini_m88@hotmail.com](mailto:cgarcini_m88@hotmail.com)
