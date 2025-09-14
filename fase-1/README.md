# Proyecto de Inteligencia Artificial: Predictor en Actividades Bancarias

**Fecha de entrega:** 21 de agosto de 2025  
**Asignatura:** Técnicas en Inteligencia Artificial  
**Estudiante:** Omar Alberto Torres  
**Docentes:** Raúl Ramos Pollán, Jonathan Granda  
**Universidad:** Universidad de Antioquia  

## Descripción del Proyecto
Este proyecto implementa un modelo de **Machine Learning supervisado** para predecir si un cliente bancario aceptará una oferta de **depósito a plazo** tras una campaña de marketing.  

El objetivo es apoyar la toma de decisiones en estrategias comerciales, priorizando clientes con mayor probabilidad de conversión y reduciendo costos de campañas ineficientes.

## Fuente de Datos
- **Dataset:** Binary Classification with a Bank Dataset  
- **Plataforma:** Kaggle  
- **Competencia:** Tabular Playground Series - Season 5, Episode 8  
- **Enlace:** [Kaggle - Playground Series S5E8](https://www.kaggle.com/competitions/playground-series-s5e8/overview)  

El dataset incluye variables demográficas y económicas de clientes, y la variable `y` que indica aceptación (`1`) o rechazo (`0`) del producto.

## Requisitos del Sistema

### Hardware mínimo sugerido
- Procesador de 64 bits  
- 8 GB de RAM  
- 2 GB de espacio libre en disco  

### Software
- Python 3.11.4  
- Entorno recomendado: **Google Colab** (no requiere instalación adicional)  

### Librerías utilizadas
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- joblib  

Estas librerías ya vienen instaladas en Google Colab. Si deseas ejecutar en local, instálalas con:

```bash
pip install pandas numpy scikit-learn matplotlib joblib
``` 

## Funcionamiento del Código

El notebook realiza los siguientes pasos:

1. Carga los datos desde `train.csv` y `test.csv`.
2. Exploración preliminar de los datos.
3. Limpieza y codificación de variables categóricas.
4. Entrenamiento de un modelo de clasificación con **Random Forest**.
5. Evaluación con métricas: Accuracy, ROC-AUC y PR-AUC.
6. Exportación del modelo entrenado (`modelo_entrenado.pkl`).
7. Generación del archivo `submission.csv` con predicciones sobre el conjunto de prueba.

## Limitaciones actuales

- No incluye validación cruzada ni optimización de hiperparámetros.  
- No incorpora técnicas avanzadas de ingeniería de características.  
- No está dockerizado ni expuesto como servicio web (fase futura).  

## Cómo Ejecutar el Proyecto

1. **Clonar el repositorio** (no descargar como ZIP, ya que se usa Git LFS):
```bash
git clone https://github.com/usuario/proyecto.git
cd proyecto
```  
Si no instalas Git LFS, los archivos .csv y .pkl aparecerán como punteros inválidos. 

2. **Abrir el notebook en Google Colab:**

   - Subir `modelo_predictor_banco.ipynb`.
   - Subir también los archivos `train.csv` y `test.csv` al entorno de Colab antes de ejecutar el código.
   - Ejecutar las celdas en orden:
     1. Carga de datos
     2. Preprocesamiento
     3. Entrenamiento
     4. Evaluación
     5. Exportación del modelo

## Contacto
Para dudas o contribuciones:

**Omar Alberto Torres**  
Correo: omara.torres@udea.edu.co  
Cel: 3043440112  


