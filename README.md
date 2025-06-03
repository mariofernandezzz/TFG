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
│ ├── mining_digcomp.ipynb # Minería de textos para DigComp
│ ├── compare_to_digcomp.ipynb # Comparación de textos externos con DigComp
│ ├── mining_esco.ipynb # Minería de textos para ESCO
│ └── compare_to_esco.ipynb # Comparación de textos externos con ESCO
├── utils/
│ ├── requirements.txt # Fichero con las bibliotecas a instalar
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

1. Clona el repositorio
Abre una terminal y clona el repositorio:

```
git clone https://github.com/tu_usuario/TFG.git
cd TFG 
```
2. Instala las dependencias
Asegúrate de tener pip actualizado, y luego instala todo lo necesario:
```
pip install --upgrade pip
pip install -r requirements.txt
```
3. Descarga el modelo de spaCy
Uno de los notebooks usa el modelo grande en inglés. Descárgalo con:
```
python -m spacy download en_core_web_lg
```
4. Abre los notebooks
Puedes abrir cualquier notebook desde la carpeta notebooks/ usando Jupyter:
```
jupyter notebook
```
o, si usas VS Code:

Abre la carpeta del proyecto.

Ve al archivo deseado en notebooks/ y ábrelo como notebook interactivo.

5. Ejecuta los notebooks
Todos los notebooks están preparados para funcionar con rutas relativas, por lo que puedes ejecutar las celdas en orden sin necesidad de modificar las rutas.

**AVISO**: El código se ha desarrollado con Python 3.12.8, por lo que se recomienda el uso de esta versión para la ejecución del código y evitar fallos.

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
