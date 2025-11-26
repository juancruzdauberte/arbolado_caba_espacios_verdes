# Análisis del Arbolado en Espacios Verdes de Buenos Aires

## 📊 Descripción del Proyecto

Este proyecto presenta un análisis del arbolado en los espacios verdes de la Ciudad Autónoma de Buenos Aires, Argentina. El análisis se centra en comprender la distribución, características y diversidad de los árboles plantados en parques y plazas de la ciudad.

## 🎯 Objetivos del Análisis

- Analizar la distribución de alturas de los árboles en espacios verdes
- Identificar las especies más comunes y sus características
- Estudiar la distribución de diámetros de tronco
- Visualizar patrones y tendencias en el arbolado urbano

## 📁 Estructura del Proyecto

```
arboles_ba_analytics/
├── arbolado.ipynb                    # Notebook principal con el análisis
├── arbolado-en-espacios-verdes.csv  # Dataset principal (13.8 MB)
├── comunas_wgs84.shp                 # Archivo shapefile de comunas
├── comunas_wgs84.shx                 # Índice del shapefile
└── README.md                         # Este archivo
```

## 📈 Dataset

El dataset contiene **51,502 registros** de árboles con las siguientes características:

### Columnas del Dataset

| Columna      | Tipo    | Descripción                           |
| ------------ | ------- | ------------------------------------- |
| `long`       | float64 | Longitud geográfica                   |
| `lat`        | float64 | Latitud geográfica                    |
| `id_arbol`   | int64   | Identificador único del árbol         |
| `altura_tot` | int64   | Altura total del árbol (metros)       |
| `diametro`   | int64   | Diámetro del tronco (cm)              |
| `inclinacio` | int64   | Inclinación del árbol                 |
| `id_especie` | int64   | Identificador de la especie           |
| `nombre_com` | object  | Nombre común de la especie            |
| `nombre_cie` | object  | Nombre científico                     |
| `tipo_folla` | object  | Tipo de follaje                       |
| `espacio_ve` | object  | Espacio verde donde se encuentra      |
| `ubicacion`  | object  | Ubicación específica                  |
| `nombre_fam` | object  | Familia botánica                      |
| `nombre_gen` | object  | Género botánico                       |
| `origen`     | object  | Origen de la especie (Nativo/Exótico) |
| `coord_x`    | float64 | Coordenada X proyectada               |
| `coord_y`    | float64 | Coordenada Y proyectada               |

### Calidad de los Datos

- **Completitud**: 51,502 registros sin valores nulos en la mayoría de columnas
- **Excepción**: La columna `ubicacion` tiene 50,529 valores no nulos (973 valores faltantes)
- **Tamaño**: 6.7+ MB en memoria

## 🔍 Análisis Realizados

### 1. Distribución de Alturas

Se analizó la distribución de las alturas totales de los árboles en los espacios verdes de CABA mediante un histograma con 40 bins. El análisis revela:

- Rango de alturas observado
- Concentración de árboles por rangos de altura
- Patrones de distribución del arbolado urbano

### 2. Especies Más Altas

Se identificaron las **10 especies de árboles más altos** y se visualizó la distribución de sus alturas mediante gráficos de violín, mostrando:

- Variabilidad de alturas dentro de cada especie
- Comparación entre especies
- Identificación de especies dominantes en altura

### 3. Distribución de Diámetros

Análisis de la distribución de diámetros de tronco mediante histograma, revelando:

- Rangos de diámetros más comunes
- Estructura etaria del arbolado (árboles jóvenes vs. maduros)
- Patrones de crecimiento

### 4. Densidad de árboles por comuna

Se analizó la distribución de los árboles por comuna en los espacios verdes de CABA mediante un mapa coroplético de calor. El análisis revela:

- Densidad de árboles por comuna
- Comunas con mayor concentración de árboles
- Comunas con menor concentración de árboles

### 5. Calidad del espacio verde

Se analizó la calidad del espacio verde en los espacios verdes de CABA mediante un mapa coroplético. El análisis revela:

- Calidad del espacio verde por comuna
- Comunas con mayor calidad de espacio verde
- Comunas con menor calidad de espacio verde

### 6. Distribución de alturas de árboles por comuna

Se analizó la distribución de las alturas totales de los árboles en los espacios verdes de CABA mediante un mapa coroplético. El análisis revela:

- Alturas totales de los árboles por comuna
- Comunas con mayor altura de árboles
- Comunas con menor altura de árboles

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Pandas**: Manipulación y análisis de datos
- **Matplotlib**: Visualizaciones estáticas
- **Seaborn**: Visualizaciones estadísticas avanzadas
- **GeoPandas**: Análisis de datos geoespaciales
- **Shapely**: Operaciones geométricas
- **Plotly**: Visualizaciones interactivas

## 📊 Visualizaciones Generadas

1. **Histograma de Alturas**: Distribución general de alturas de todos los árboles
2. **Gráficos de Violín**: Distribución de alturas de las 10 especies más altas
3. **Histograma de Diámetros**: Distribución de diámetros de tronco
4. **Mapa de calor**: Densidad de árboles por comuna
5. **Mapa de árbol**: Cantidad de árboles
6. **Mapas coropléticos**: Calidad del espacio verde y distribución de la altura de los árboles por comuna

## 💡 Insights Principales

- El dataset representa una muestra significativa del arbolado urbano de Buenos Aires
- Se observa una gran diversidad de especies arbóreas
- Las visualizaciones permiten identificar patrones en la estructura del arbolado urbano
- Los datos geoespaciales facilitan análisis de distribución territorial

## 📝 Notas Técnicas

- El análisis utiliza coordenadas geográficas en formato WGS84
- Los datos de comunas están disponibles en formato shapefile

---

**Fuente de datos**: Gobierno de la Ciudad de Buenos Aires - Datos Abiertos
