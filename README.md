# Trabajo de Fin de Grado – Minería de texto aplicada a estándares, marcos y documentos de referencia educativos y competenciales en el ámbito de la informática

Este repositorio contiene el código, datos y recursos utilizados para el desarrollo del TFG, centrado en la **identificación de competencias asociadas a textos** mediante la comparación con los marcos **DigComp** y **ESCO**. El análisis se basa en técnicas de **minería de texto**, **representación semántica** y **similitud por frecuencia léxica**.

---

## 📁 Estructura del repositorio

```
TFG/
├── data/
│ ├── digcomp/
│ │ └── *.csv # Archivos de tablas usadas de DigComp y base de datos Access
│ └── esco/
│ └── *.csv # Archivos de la única tabla de ESCO que pasó por diferentes fases
├── notebooks/
│ ├── requirements.txt # Fichero con las bibliotecas a instalar
│ ├── mining_digcomp.ipynb # Minería de textos para DigComp
│ ├── compare_to_digcomp.ipynb # Comparación de textos externos con DigComp
│ ├── mining_esco.ipynb # Minería de textos para ESCO
│ └── compare_to_esco.ipynb # Comparación de textos externos con ESCO
├── utils/
│ ├── mapping.csv # Archivo de mapeo léxico
│ ├── tokens_revisar_digcomp.csv # Tokens a revisar (DigComp)
│ └── tokens_revisar_esco.csv # Tokens a revisar (ESCO)
├── results/
│ ├── digcomp/
│ │ ├── *.csv # 7 matrices de frecuencias
│ │ ├── results_digcomp.x # Fichero con los resultados de filtrado de minería de texto
│ └── esco/
│   ├── frecuencias_esco.csv # Matriz de frecuencia
│   ├── results_esco.x # Fichero con los resultados de filtrado de minería de texto
├── README.md # Descripción general del proyecto
```


---

## ⚙️ Cómo ejecutar el código en Google Colab

Puedes usar directamente los notebooks desde Google Colab con los siguientes pasos:

1. Abre un notebook de `notebooks/` en Google Colab (ej. `compare_to_digcomp.ipynb`).
2. En la primera celda, clona el repositorio:

```python
!git clone https://github.com/tu_usuario/TFG.git
%cd TFG
```

3. Asegúrate de que las rutas relativas funcionen (los notebooks ya están preparados para eso).

4. Ejecuta las celdas en orden. El código procesará el texto, lo mapeará y lo comparará con los grupos de competencias usando matrices de frecuencia.

## 🧩 Funcionalidades principales
- Tokenización, eliminación de stopwords y lematización con spaCy.

- Mapeo léxico personalizado para unificar términos relacionados.

- Comparación por similitud coseno entre textos y grupos de competencia.

- Identificación de palabras clave más relevantes por grupo.

- Salida estructurada y ordenada para facilitar el análisis interpretativo.

## 📚 Marcos de referencia utilizados
- **DigComp** (Marco Europeo de Competencias Digitales)

- **ESCO** (Clasificación Europea de Competencias, Cualificaciones y Ocupaciones)

## 📝 Autor
Mario Fernández Rueda \
Grado en Ingeniería Informática – Universidad de Alcalá
