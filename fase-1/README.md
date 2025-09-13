#  Proyecto de Inteligencia Artificial: Predictor en Actividades Bancarias

**Fecha de entrega:** 21 de agosto de 2025  
**Asignatura:**  Técnicas en Inteligencia Artificial  
**Estudiante**   Omar Alberto Torres
**Docentes:**     Raúl Ramos Pollán,  Jonathan Granda
**Universidad:** Universidad de Antioquia

---

##  Descripción del Proyecto

Este proyecto consiste en el desarrollo de un modelo de **Machine Learning supervisado** para predecir si un cliente bancario aceptará una oferta de **depósito a plazo** tras una campaña de marketing.  
El objetivo es facilitar la toma de decisiones en estrategias comerciales, priorizando contactos con mayor probabilidad de conversión y reduciendo costos de campañas ineficientes.

---

## Fuente de Datos

- **Nombre del dataset:** Binary Classification with a Bank Dataset  
- **Plataforma:** Kaggle  
- **Competencia:** Tabular Playground Series - Season 5, Episode 8  
- **Enlace al dataset:** [https://www.kaggle.com/competitions/playground-series-s5e8/overview](https://www.kaggle.com/competitions/playground-series-s5e8/overview)

El conjunto de datos incluye características demográficas y económicas de clientes, junto con el resultado (`y`) que indica si el cliente aceptó el producto bancario (`1`) o no (`0`).

---

## Requisitos del Sistema

### Hardware mínimo sugerido
- Procesador de 64 bits
- 8 GB de RAM
- 2 GB de espacio libre en disco

### Software necesario
- Python 3.11.4
- Entorno recomendado: Google Colab o Jupyter Notebook
- Librerías requeridas:
  a. bash
  b. pandas
  c. numpy
  d. scikit-learn
  e. matplotlib
  f. joblib

### Puedes instalar las librerías asi:
pip install pandas numpy scikit-learn matplotlib joblib

### Funcionamiento del código: 
¿Qué hace este código?

a. Carga los datos desde train.csv y test.csv.
b. Realiza una exploración preliminar de los datos.
c. Aplica limpieza y codificación de variables categóricas.
d. Entrena un modelo de clasificación basado en Random Forest.
e. Evalúa el modelo con métricas como Accuracy, ROC-AUC y PR-AUC.
f. Guarda el modelo entrenado (modelo_entrenado.pkl) para futuras predicciones.
g. Genera un archivo submission.csv con predicciones sobre el conjunto test.

## ¿Qué no hace este código?
a. No realiza un análisis profundo de correlación o ingeniería avanzada de características.
b. No implementa validación cruzada ni optimización de hiperparámetros.
c. No está aún dockerizado ni expuesto como servicio web (esto se desarrollará en fases posteriores).
d. No incluye visualización de interpretabilidad del modelo.

## Cómo Ejecutar el Proyecto
a. Descarga o clona este repositorio.
b. Abre el archivo modelo_predictor_banco.ipynb en Google Colab o Jupyter Notebook.
c. Ejecuta las celdas secuencialmente:
d. Carga de datos
e. Análisis y preprocesamiento
f. Entrenamiento del modelo
g. Evaluación
h. Exportación del modelo
i. (Opcional) Descarga el modelo entrenado para uso posterior:
   ### from google.colab import files
   ### files.download("modelo_bank_predictor.pkl") 

##  Contacto
Para dudas o contribuciones contactar:
Omar Alberto Torres
cel: 3043440112
email: omara.torres@udea.edu.co

# Gestión de archivos grandes con Git LFS

Este proyecto requiere el uso de archivos grandes (.csv) que exceden el límite de tamaño estándar de GitHub.  
Para garantizar su correcto funcionamiento, se utilizó Git LFS (Large File Storage).

### Archivos incluidos con LFS:
- fase-1/train.csv (~62 MB) – Dataset de entrenamiento
- fase-1/modelo_entrenado.pkl (~180 MB) – Modelo de clasificación entrenado

### ¿Qué se hizo?

1. Se instaló Git LFS en Windows desde: https://git-lfs.github.com
2. Se inicializó Git LFS:
   ```bash
   git lfs install

## Para manejo de archivos *.csv  y *.pkl de ser necesario use los siguientes comandos previo a tener 
## Instaladdo sfl
git lfs track "*.csv"
git lfs track "*.pkl"
git add .gitattributes

## En caso de ser necesario limpiar historia de commit puede ejecutarse el comando
## Se limpiaron los commits antiguos y se migraron los archivos al sistema LFS:
git lfs migrate import --include="*.csv"

## Recomendaciones para clonar este repositorio
Antes de clonar o usar este repositorio, instala Git LFS en tu máquina.
De lo contrario, los archivos .csv y  se verán como referencias inválidas (punteros).

## Se descargo lfs asi
# Paso demasiado importante
Durante La creación del repositorio en Github fue necesario instalar la herramienta "Git Large storage"
Segun sea el sistema operativo debes instalar lsf, ejecutar git-lfs-windows-v3.7.0 (Mi equipo tiene sistema operativo windos)

1. Se instaló Git LFS en Windows descargando el instalador desde: https://git-lfs.github.com
2. se ejecuto: git-lfs-windows-v3.7.0.exe
3. Luego se ejecutó:
   ejecute git lfs --version (para ver version instalada)
   git lfs install  (inicializa)
   Clonar el repositorio (Es muy importante no hacer descarga ZIP, debe clonarse el repositorio)




